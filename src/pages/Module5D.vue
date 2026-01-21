<template>
    <div>
        <v-row>
            <template v-if="klipperReadyForGui">
                <v-col class="col-12 col-md-8 pb-0">
                    <wcs-graph />
                </v-col>
                <v-col class="col-12 col-md-4">
                    <toolhead-control-panel />
                    <module5d-control-panel />
                </v-col>
            </template>

            <template v-else>
                <v-col>
                    <v-alert
                        dense
                        text
                        type="warning"
                        elevation="2"
                        class="mx-auto mt-6"
                        max-width="500"
                        :icon="mdiLockOutline">
                        {{ $t('Module5d.ErrorKlipperNotReady') }}
                    </v-alert>
                </v-col>
            </template>
        </v-row>
    </div>
</template>
<script lang="ts">
import { Component, Mixins } from 'vue-property-decorator'
import BaseMixin from '@/components/mixins/base'

import Panel from '@/components/ui/Panel.vue'
import ToolheadControlPanel from '@/components/panels/ToolheadControlPanel.vue'
import Module5dControlPanel from '@/components/panels/Module5dControlPanel.vue'
import { mdiLockOutline } from '@mdi/js'

@Component({
    components: { Panel, ToolheadControlPanel, Module5dControlPanel },
})
export default class PageModule5D extends Mixins(BaseMixin) {
    mdiLockOutline = mdiLockOutline
}
</script>
