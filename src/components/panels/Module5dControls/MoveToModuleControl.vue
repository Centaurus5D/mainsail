<template>
    <v-container v-if="showCoordinates || showPosition" :class="containerClass">
        <responsive
            :breakpoints="{
                xsmall: (el) => el.width <= 320,
                small: (el) => el.width > 320 && el.width <= 460,
                medium: (el) => el.width > 460 && el.width <= 560,
                large: (el) => el.width > 560,
            }">
            <template #default="{ el }">
                <v-row v-if="needCalibration" justify="center">
                    <v-alert dense text type="warning" elevation="2" class="mx-2 mt-6">
                        {{ $t('Module5d.ModuleNotCalibrated') }}
                    </v-alert>
                </v-row>
                <v-row v-if="showPosition" class="flex-nowrap pb-1">
                    <v-col class="col-12 v-subheader text--secondary mr-2">
                        <v-icon small class="mr-1">{{ mdiCrosshairsGps }}</v-icon>
                        <span v-if="!el.is.xsmall" class="text-no-wrap">
                            {{ $t('Panels.ToolheadControlPanel.Position') }}:&nbsp;
                        </span>
                        <span class="text-no-wrap">{{ displayPositionAbsolute }}</span>
                    </v-col>
                </v-row>
                <v-row v-if="showCoordinates" dense>
                    <v-col :class="el.is.xsmall ? 'col-12' : 'col-6'">
                        <move-to-input
                            v-model="input.a.pos"
                            :label="livePositions.a"
                            :suffix="'A'"
                            :step="0.01"
                            :current-pos="gcodePositions.a"
                            :readonly="['printing'].includes(printer_state)"
                            :disabled="!aAxisHomed"
                            @submit="sendCmd" />
                    </v-col>
                    <v-col :class="el.is.xsmall ? 'col-12' : 'col-6'">
                        <move-to-input
                            v-model="input.c.pos"
                            :label="livePositions.c"
                            :suffix="'C'"
                            :step="0.01"
                            :current-pos="gcodePositions.c"
                            :readonly="['printing'].includes(printer_state)"
                            :disabled="!cAxisHomed"
                            @submit="sendCmd" />
                    </v-col>
                </v-row>
            </template>
        </responsive>
    </v-container>
</template>

<script lang="ts">
import { Component, Mixins, Watch } from 'vue-property-decorator'
import BaseMixin from '@/components/mixins/base'
import ControlMixin from '@/components/mixins/control'
import MoveToInput from '@/components/inputs/MoveToInput.vue'
import Responsive from '@/components/ui/Responsive.vue'
import { mdiCrosshairsGps } from '@mdi/js'

@Component({
    components: { MoveToInput, Responsive },
})
export default class MoveToModuleControl extends Mixins(BaseMixin, ControlMixin) {
    mdiCrosshairsGps = mdiCrosshairsGps

    input: { [index: string]: any } = {
        a: { pos: '', valid: true },
        c: { pos: '', valid: true },
    }

    @Watch('gcodePositions.a', { immediate: true })
    updatePositionA(newVal: string): void {
        this.input.a.pos = newVal
    }

    @Watch('gcodePositions.c', { immediate: true })
    updatePositionC(newVal: string): void {
        this.input.c.pos = newVal
    }

    get aAxisHomed(): boolean {
        const homed = this.$store.state.printer.module_5d?.toolhead.homed_axes ?? ""
        return homed.includes('a')
    }

    get cAxisHomed(): boolean {
        const homed = this.$store.state.printer.module_5d?.toolhead.homed_axes ?? ""
        return homed.includes('c')
    }

    /**
     * Axes positions and positioning mode (G90 / G91)
     */
    get displayPositionAbsolute() {
        return this.positionAbsolute
            ? this.$t('Panels.ToolheadControlPanel.Absolute')
            : this.$t('Panels.ToolheadControlPanel.Relative')
    }

    get positionAbsolute() {
        return this.$store.state.printer.gcode_move?.absolute_coordinates ?? true
    }

    get gcodePositions() {
        const pos = this.$store.state.printer.module_5d?.gcode_position ?? [0, 0]
        return {
            a: pos[0]?.toFixed(2) ?? '--',
            c: pos[1]?.toFixed(2) ?? '--',
        }
    }

    get livePositions() {
        const pos = this.$store.state.printer.module_5d?.position ?? [0, 0]
        return {
            a: pos[0]?.toFixed(2) ?? '--',
            c: pos[1]?.toFixed(2) ?? '--',
        }
    }

    get showPosition() {
        return this.$store.state.gui.view.module5d.showPosition ?? true
    }

    get showCoordinates() {
        return this.$store.state.gui.view.module5d.showCoordinates ?? true
    }

    get showControl() {
        return this.$store.state.gui.view.module5d.showControl ?? true
    }

    get containerClass() {
        return this.showControl ? 'pb-0' : ''
    }

    sendCmd(): void {
        let gcode: string[] = []
        if (!this.existsClientLinearMoveMacro) {
            gcode.push('SAVE_GCODE_STATE NAME=_ui_movement')
            gcode.push('G90')
        }

        if (this.input.a.pos !== this.gcodePositions.a || this.input.c.pos !== this.gcodePositions.c) {
            let aPos = ''
            let cPos = ''

            if (this.existsClientLinearMoveMacro) {
                if (this.input.a.pos !== this.gcodePositions.a) aPos = ` A=${this.input.a.pos}`
                if (this.input.c.pos !== this.gcodePositions.c) cPos = ` C=${this.input.c.pos}`

                gcode.push(`_CLIENT_LINEAR_MOVE${aPos}${cPos} F=${this.feedrateXY * 60} ABSOLUTE=1`)
            } else {
                if (this.input.a.pos !== this.gcodePositions.a) aPos = ` A${this.input.a.pos}`
                if (this.input.c.pos !== this.gcodePositions.c) cPos = ` C${this.input.c.pos}`

                gcode.push(`G1${aPos}${cPos} F${this.feedrateXY * 60}`)
            }
        }

        if (!this.existsClientLinearMoveMacro) {
            gcode.push('RESTORE_GCODE_STATE NAME=_ui_movement')
        }

        const gcodeStr = gcode.join('\n')

        if (this.input.a.valid && this.input.c.valid) {
            this.$store.dispatch('server/addEvent', { message: gcodeStr, type: 'command' })
            this.$socket.emit('printer.gcode.script', { script: gcodeStr })
        }

        return
    }

    get wcsOffsets() {
        return (
            this.$store.state.printer.module_5d.wcs_offsets ?? [
                [0, 0, 0],
                [0, 0, 0],
                [0, 0, 0],
                [0, 0, 0],
                [0, 0, 0],
            ]
        )
    }

    get needCalibration() {
        const baseWcs1 = Object.values(this.$store.state.printer.configfile?.settings?.wcs_1) ?? []
        const baseWcs2 = Object.values(this.$store.state.printer.configfile?.settings?.wcs_2) ?? []
        return (
            baseWcs1.every((v, i) => v === this.wcsOffsets[1][i]) ||
            baseWcs2.every((v, i) => v === this.wcsOffsets[2][i])
        )
    }
}
</script>
