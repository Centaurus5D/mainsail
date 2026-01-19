<template>
    <div>
        <!-- HOME ALL / ACTION BUTTON -->
        <v-row no-gutters>
            <v-col class="col-12 pb-0 text-center">
                <v-btn
                    small
                    :disabled="['printing'].includes(printer_state)"
                    :loading="loadings.includes('homeModuleAll')"
                    :color="homedAxes.includes('ac') ? 'primary' : 'warning'"
                    @click="doHomeModule">
                    <v-icon class="mr-1">{{ mdiHome }}</v-icon>
                    {{ $t('Panels.ToolheadControlPanel.ALL') }}
                </v-btn>
                <v-btn
                    small
                    :disabled="['printing'].includes(printer_state)"
                    :color="homedAxes !== '' ? 'primary' : 'warning'"
                    class="ml-2"
                    @click="doSend('M84')">
                    <v-icon>{{ mdiEngineOff }}</v-icon>
                </v-btn>
            </v-col>
        </v-row>
        <!-- A MOVEMENT BUTTONGROUPS -->
        <v-row dense>
            <v-col class="text-center">
                <v-item-group class="_btn-group row no-gutters">
                    <v-btn
                        v-for="steps of stepsXYsorted"
                        :key="'a-' + steps"
                        :disabled="['printing'].includes(printer_state)"
                        class="btnMinWidthAuto col btnGroup"
                        @click="doSendMove('A-' + steps, feedrateXY)">
                        <span class="body-2">–{{ steps }}</span>
                    </v-btn>
                    <v-btn
                        :disabled="['printing'].includes(printer_state)"
                        :color="homedAxes.includes('a') ? 'primary' : 'warning'"
                        :loading="loadings.includes('homeA')"
                        class="font-weight-bold btnHomeAxis btnGroup"
                        @click="doHomeA">
                        A
                    </v-btn>
                    <v-btn
                        v-for="steps of stepsXYsortedReverse"
                        :key="'a+' + steps"
                        :disabled="['printing'].includes(printer_state)"
                        class="btnMinWidthAuto col btnGroup"
                        @click="doSendMove('A+' + steps, feedrateXY)">
                        <span class="body-2">+{{ steps }}</span>
                    </v-btn>
                </v-item-group>
            </v-col>
        </v-row>
        <!-- C MOVEMENT BUTTONGROUPS -->
        <v-row dense>
            <v-col class="text-center">
                <v-item-group class="_btn-group row no-gutters">
                    <v-btn
                        v-for="steps of stepsXYsorted"
                        :key="'c-' + steps"
                        :disabled="['printing'].includes(printer_state)"
                        class="btnMinWidthAuto col btnGroup"
                        @click="doSendMove('C-' + steps, feedrateXY)">
                        <span class="body-2">–{{ steps }}</span>
                    </v-btn>
                    <v-btn
                        :disabled="['printing'].includes(printer_state)"
                        :color="homedAxes.includes('c') ? 'primary' : 'warning'"
                        :loading="loadings.includes('homeC')"
                        class="font-weight-bold btnHomeAxis btnGroup"
                        @click="doHomeC">
                        C
                    </v-btn>
                    <v-btn
                        v-for="steps of stepsXYsortedReverse"
                        :key="'c+' + steps"
                        :disabled="['printing'].includes(printer_state)"
                        class="btnMinWidthAuto col btnGroup"
                        @click="doSendMove('C+' + steps, feedrateXY)">
                        <span class="body-2">+{{ steps }}</span>
                    </v-btn>
                </v-item-group>
            </v-col>
        </v-row>
    </div>
</template>

<script lang="ts">
import { Component, Mixins } from 'vue-property-decorator'
import BaseMixin from '@/components/mixins/base'
import ControlMixin from '@/components/mixins/control'
import { mdiEngineOff, mdiHome } from '@mdi/js'

@Component
export default class Module5dBarsControl extends Mixins(BaseMixin, ControlMixin) {
    mdiEngineOff = mdiEngineOff
    mdiHome = mdiHome

    get homedAxes(): string {
        return this.$store.state.printer?.module_5d.toolhead?.homed_axes ?? ''
    }

    doHomeA() {
        this.$store.dispatch('server/addEvent', { message: 'HOME_MODULE A=1', type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: 'HOME_MODULE A=1' }, { loading: 'homeA' })
    }

    doHomeC() {
        this.$store.dispatch('server/addEvent', { message: 'HOME_MODULE C=1', type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: 'HOME_MODULE C=1' }, { loading: 'homeC' })
    }

    doHomeModule() {
        this.$store.dispatch('server/addEvent', { message: 'HOME_MODULE', type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: 'HOME_MODULE' }, { loading: 'homeModuleAll' })
    }

    get stepsXYsorted() {
        return [...this.$store.state.gui.control.stepsXY].sort(function (a, b) {
            return b - a
        })
    }

    get stepsXYsortedReverse() {
        return [...this.$store.state.gui.control.stepsXY].sort(function (a, b) {
            return a - b
        })
    }
}
</script>

<style scoped>
.btnHomeAxis {
    width: 36px;
    min-width: 36px !important;
}

.btnGroup {
    height: 28px !important;
}

.btnMinWidthAuto {
    min-width: auto !important;
}

._btn-group {
    border-radius: 4px;
    display: inline-flex;
    flex-wrap: nowrap;
    max-width: 100%;
    min-width: 100%;
    width: 100%;

    .v-btn {
        border-radius: 0;
        border-color: rgba(255, 255, 255, 0.12);
        border-style: solid;
        border-width: thin;
        box-shadow: none;
        height: 28px;
        opacity: 0.8;
        min-width: auto !important;
    }

    .v-btn:first-child {
        border-top-left-radius: inherit;
        border-bottom-left-radius: inherit;
    }

    .v-btn:last-child {
        border-top-right-radius: inherit;
        border-bottom-right-radius: inherit;
    }

    .v-btn:not(:first-child) {
        border-left-width: 0;
    }
}

html.theme--light ._btn-group .v-btn {
    border-color: rgba(0, 0, 0, 0.12);
}
</style>
