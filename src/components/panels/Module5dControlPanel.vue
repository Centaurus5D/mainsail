<template>
    <panel
        v-if="klipperReadyForGui"
        :icon="mdiNumeric5CircleOutline"
        :title="$t('Panels.Module5dControlPanel.Headline')"
        :collapsible="true"
        card-class="module5d-control-panel">
        <!-- PANEL-HEADER 3-DOT-MENU -->
        <template #buttons>
            <module5d-panel-settings />
        </template>
        <!-- MOVE TO CONTROL -->
        <move-to-module-control />
        <!-- AXIS CONTROL -->
        <v-container v-if="axisControlVisible">
            <component :is="`bars-control`" />
        </v-container>
    </panel>
</template>

<script lang="ts">
import { Component, Mixins } from 'vue-property-decorator'
import BarsControl from '@/components/panels/Module5dControls/BarsControl.vue'
import BaseMixin from '../mixins/base'
import ControlMixin from '@/components/mixins/control'
import MoveToModuleControl from '@/components/panels/Module5dControls/MoveToModuleControl.vue'
import Panel from '@/components/ui/Panel.vue'
import {
    mdiDotsVertical,
    mdiEngineOff,
    mdiNumeric5CircleOutline,
    mdiSpeedometer,
    mdiMenuDown,
    mdiRestore,
} from '@mdi/js'

@Component({
    components: {
        BarsControl,
        MoveToModuleControl,
        Panel,
    },
})
export default class Module5dControlPanel extends Mixins(BaseMixin, ControlMixin) {
    mdiDotsVertical = mdiDotsVertical
    mdiEngineOff = mdiEngineOff
    mdiNumeric5CircleOutline = mdiNumeric5CircleOutline
    mdiSpeedometer = mdiSpeedometer
    mdiRestore = mdiRestore
    mdiMenuDown = mdiMenuDown

    get controlStyle(): string {
        return this.$store.state.gui.control.style ?? 'bars'
    }

    get actionButton(): string {
        return this.$store.state.gui.control.actionButton ?? this.defaultActionButton
    }

    get isPrinting() {
        return ['printing'].includes(this.printer_state)
    }

    get axisControlVisible() {
        if (!this.showControl) return false

        return !(this.isPrinting && (this.$store.state.gui.control.hideDuringPrint ?? false))
    }

    get showControl(): boolean {
        return this.$store.state.gui.view.module5d.showControl ?? true
    }
}
</script>
