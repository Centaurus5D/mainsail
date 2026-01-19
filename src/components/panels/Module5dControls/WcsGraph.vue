<template>
    <panel :icon="mdiChartLine" :title="$t('Panels.Module5dControlPanel.WcsGraph')" :collapsible="true"></panel>
</template>

<script lang="ts">
import { Component, Mixins } from 'vue-property-decorator'
import BaseMixin from '@/components/mixins/base'
import Panel from '@/components/ui/Panel.vue'
import { mdiChartLine } from '@mdi/js'

@Component({
    components: {
        Panel,
    },
})
export default class WcsGraph extends Mixins(BaseMixin) {}
</script>

<style scoped></style>
