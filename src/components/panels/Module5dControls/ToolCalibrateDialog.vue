<template>
    <v-dialog v-model="showDialog" persistent :max-width="400" @keydown.esc="closeDialog">
        <panel
            :title="$t('Module5d.TitleCalibrate')"
            :icon="mdiChartLineVariant"
            card-class="module5d-calibrate-dialog"
            :margin-bottom="false">
            <template #buttons>
                <v-btn icon tile @click="closeDialog">
                    <v-icon>{{ mdiCloseThick }}</v-icon>
                </v-btn>
            </template>
            <v-card-text>
                <v-text-field
                    ref="input"
                    v-model="radius"
                    type="number"
                    :label="$t('Module5d.ToolRadius')"
                    required
                    :rules="rules"
                    @update:error="
                        (newVal) => {
                            isInvalidRadius = newVal
                        }
                    "
                    @keyup.enter="calibrateMesh" />
            </v-card-text>
            <v-card-actions>
                <v-spacer />
                <v-btn text @click="closeDialog">{{ $t('Buttons.Cancel') }}</v-btn>
                <v-btn :disabled="isInvalidRadius" color="primary" text @click="calibrateMesh">
                    {{ $t('Heightmap.Calibrate') }}
                </v-btn>
            </v-card-actions>
        </panel>
    </v-dialog>
</template>
<script lang="ts">
import { Component, Mixins, Ref, VModel, Watch } from 'vue-property-decorator'
import BaseMixin from '@/components/mixins/base'
import { mdiCloseThick, mdiChartLineVariant } from '@mdi/js'

@Component
export default class ToolCalibrateDialog extends Mixins(BaseMixin) {
    mdiCloseThick = mdiCloseThick
    mdiChartLineVariant = mdiChartLineVariant

    @VModel({ type: Boolean }) showDialog!: boolean
    @Ref() input!: HTMLInputElement

    isInvalidRadius = false
    radius = 0.0

    get rangeZ(): number[] {
        const axis_minimum = this.$store.state.printer.toolhead?.axis_minimum
        const axis_maximum = this.$store.state.printer.toolhead?.axis_maximum

        return [axis_minimum[2] ?? 0, axis_maximum[2] ?? 0]
    }

    get absRangeZ(): number {
        return this.rangeZ[1] - this.rangeZ[0]
    }

    rules = [
        (value: number) => !!value || this.$t('Heightmap.InvalidNameEmpty'),
        //Must be lower than wcs 2 z that shows
        (value: number) => (value > 0 && value < this.absRangeZ / 2) || this.$t('Module5d.InvalidRadius'),
    ]

    calibrateMesh(): void {
        const gcode = `TOOL_CALIBRATE TOOL_RADIUS=${this.radius}`

        this.$store.dispatch('server/addEvent', { message: gcode, type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: gcode }, { loading: 'bedMeshCalibrate' })

        this.closeDialog()
    }

    closeDialog() {
        this.showDialog = false
    }

    @Watch('showDialog')
    onShowDialogChanged(newVal: boolean) {
        if (!newVal) return

        this.radius = 3.0
        setTimeout(() => {
            this.input?.focus()
        })
    }
}
</script>
