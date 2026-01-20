<template>
    <panel :icon="mdiChartLineVariant" :title="$t('Panels.Module5dControlPanel.WcsGraph')" card-class="wcs-graph">
        <template #buttons>
            <v-btn
                icon
                tile
                class="d-none d-sm-flex"
                :disabled="printerIsPrinting"
                :color="homedAxes.includes('xyz') ? 'primary' : 'warning'"
                :loading="loadings.includes('homeAll')"
                :title="$t('Heightmap.TitleHomeAll')"
                :ripple="true"
                @click="homePrinter">
                <v-icon>{{ mdiHome }}</v-icon>
            </v-btn>
            <v-btn
                text
                tile
                class="d-none d-sm-flex"
                :loading="loadings.includes('clearWcs')"
                :title="$t('Module5d.TitleClear')"
                @click="clearWcs">
                {{ $t('Module5D.Clear') }}
            </v-btn>
            <v-btn
                text
                tile
                class="d-none d-sm-flex"
                :loading="loadings.includes('module5dCalibrate')"
                :disabled="printerIsPrinting"
                :title="$t('Module5d.TitleCalibrate')"
                @click="calibrateDialog = true">
                {{ $t('Heightmap.Calibrate') }}
            </v-btn>
        </template>
        <v-container>
            <v-row justify="center">
                <v-col cols="12" md="10" lg="6">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        style="background: transparent; background-color: transparent; color-scheme: light"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        version="1.1"
                        width="100%"
                        height="100%"
                        viewBox="-0.5 -0.5 292 292">
                        <defs />
                        <g>
                            <g data-cell-id="0">
                                <g data-cell-id="1">
                                    <g data-cell-id="wZJ3dYeiSbHgKBZ8uvrL-6">
                                        <g />
                                        <g data-cell-id="wZJ3dYeiSbHgKBZ8uvrL-1">
                                            <g>
                                                <path
                                                    d="M 0.27 20.9 C 0.27 17.09 7.27 14 15.9 14 C 20.05 14 24.03 14.73 26.96 16.02 C 29.89 17.32 31.54 19.07 31.54 20.9 L 31.54 177.1 C 31.54 178.93 29.89 180.68 26.96 181.98 C 24.03 183.27 20.05 184 15.9 184 C 11.76 184 7.78 183.27 4.85 181.98 C 1.92 180.68 0.27 178.93 0.27 177.1 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 31.54 20.9 C 31.54 22.74 29.89 24.49 26.96 25.79 C 24.03 27.08 20.05 27.81 15.9 27.81 C 11.76 27.81 7.78 27.08 4.85 25.79 C 1.92 24.49 0.27 22.74 0.27 20.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="wZJ3dYeiSbHgKBZ8uvrL-19">
                                        <g />
                                        <g data-cell-id="wZJ3dYeiSbHgKBZ8uvrL-20">
                                            <g>
                                                <path
                                                    d="M 79.73 155.9 C 79.73 152.09 86.73 149 95.37 149 C 99.51 149 103.49 149.73 106.42 151.02 C 109.35 152.32 111 154.07 111 155.9 L 111 312.1 C 111 313.93 109.35 315.68 106.42 316.98 C 103.49 318.27 99.51 319 95.37 319 C 91.22 319 87.24 318.27 84.31 316.98 C 81.38 315.68 79.73 313.93 79.73 312.1 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(120,95.37,234)"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 111 155.9 C 111 157.74 109.35 159.49 106.42 160.79 C 103.49 162.08 99.51 162.81 95.37 162.81 C 91.22 162.81 87.24 162.08 84.31 160.79 C 81.38 159.49 79.73 157.74 79.73 155.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(120,95.37,234)"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="wZJ3dYeiSbHgKBZ8uvrL-21">
                                        <g>
                                            <path
                                                d="M 165.58 272 L 207.91 247.56 L 196.99 241.25 L 186.06 234.94 L 231 209"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                            <ellipse
                                                cx="162.98"
                                                cy="273.5"
                                                rx="3"
                                                ry="3"
                                                :fill="strokeColor"
                                                :stroke="strokeColor"
                                                pointer-events="all" />
                                        </g>
                                    </g>
                                    <g data-cell-id="wZJ3dYeiSbHgKBZ8uvrL-16">
                                        <g>
                                            <rect
                                                x="71"
                                                y="29"
                                                width="100"
                                                height="60"
                                                rx="2.4"
                                                ry="2.4"
                                                fill="none"
                                                :stroke="strokeColor"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g>
                                                <switch>
                                                    <foreignObject
                                                        style="overflow: visible; text-align: left"
                                                        pointer-events="none"
                                                        width="100%"
                                                        height="100%"
                                                        requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility">
                                                        <div
                                                            xmlns="http://www.w3.org/1999/xhtml"
                                                            style="
                                                                display: flex;
                                                                align-items: unsafe center;
                                                                justify-content: unsafe center;
                                                                width: 118px;
                                                                height: 1px;
                                                                padding-top: 59px;
                                                                margin-left: 62px;
                                                            ">
                                                            <div>
                                                                <div v-if="rows[1]" class="text-body-2">
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset.wcs === 1 &&
                                                                                hoveredOffset.axis === 0
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        {{ rows[1].X }}
                                                                    </span>
                                                                    <br />
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset.wcs === 1 &&
                                                                                hoveredOffset.axis === 1
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        {{ rows[1].Y }}
                                                                    </span>
                                                                    <br />
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset?.wcs === 1 &&
                                                                                hoveredOffset.axis === 2
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        {{ rows[1].Z }}
                                                                    </span>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="wZJ3dYeiSbHgKBZ8uvrL-23">
                                        <g>
                                            <rect
                                                x="171"
                                                y="149"
                                                width="120"
                                                height="60"
                                                rx="2.4"
                                                ry="2.4"
                                                fill="none"
                                                :stroke="strokeColor"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g>
                                                <switch>
                                                    <foreignObject
                                                        style="overflow: visible; text-align: left"
                                                        pointer-events="none"
                                                        width="100%"
                                                        height="100%"
                                                        requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility">
                                                        <div
                                                            xmlns="http://www.w3.org/1999/xhtml"
                                                            style="
                                                                display: flex;
                                                                align-items: unsafe center;
                                                                justify-content: unsafe center;
                                                                width: 118px;
                                                                height: 1px;
                                                                padding-top: 179px;
                                                                margin-left: 172px;
                                                            ">
                                                            <div>
                                                                <div v-if="rows[2]" class="text-body-2">
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset?.wcs === 2 &&
                                                                                hoveredOffset.axis === 0
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        {{ rows[2].X }}
                                                                    </span>
                                                                    <br />
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset?.wcs === 2 &&
                                                                                hoveredOffset.axis === 1
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        {{ rows[2].Y }}
                                                                    </span>
                                                                    <br />
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset?.wcs === 2 &&
                                                                                hoveredOffset.axis === 2
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        {{ rows[2].Z }}
                                                                    </span>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g>
                                        <g>
                                            <path
                                                d="M 18.5 21.5 L 37.59 32.52 L 61 19 L 82.34 6.68 L 121 29"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                            <ellipse
                                                cx="15.9"
                                                cy="20"
                                                rx="3"
                                                ry="3"
                                                :fill="strokeColor"
                                                :stroke="strokeColor"
                                                pointer-events="all" />
                                        </g>
                                    </g>
                                </g>
                            </g>
                        </g>
                    </svg>
                </v-col>
                <v-col cols="12" md="10" lg="6">
                    <responsive
                        :breakpoints="{
                            xsmall: (el) => el.width <= 320,
                            small: (el) => el.width > 320 && el.width <= 460,
                            medium: (el) => el.width > 460 && el.width <= 560,
                            large: (el) => el.width > 560,
                        }">
                        <template #default="{ el }">
                            <v-row dense>
                                <v-col :class="'col-12'">
                                    <wcs-input
                                        v-model="offsetsInput[1][0]"
                                        :label="$t('Module5d.AoffsetPanel.Headline')"
                                        :suffix="'A'"
                                        :step="0.01"
                                        :current-pos="wcsOffsets[1][0].toFixed(3)"
                                        @submit="sendCmd(1, 0)"
                                        @focus="onFocus(1, 0)"
                                        @blur="onBlur" />
                                </v-col>
                                <v-col class="col-12 v-subheader text--secondary mr-2">
                                    <span v-if="!el.is.xsmall" class="text-no-wrap">WCS 1</span>
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        v-model="offsetsInput[1][0]"
                                        label="WCS 1"
                                        :suffix="'X'"
                                        :step="0.01"
                                        :current-pos="wcsOffsets[1][0].toFixed(3)"
                                        @submit="sendCmd(1, 0)"
                                        @focus="onFocus(1, 0)"
                                        @blur="onBlur" />
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        :value="wcsOffsets[1][1].toFixed(3)"
                                        label="WCS 1"
                                        :suffix="'Y'"
                                        :step="0.01"
                                        :current-pos="wcsOffsets[1][1].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(1, 1)"
                                        @blur="onBlur" />
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        :value="wcsOffsets[1][2].toFixed(3)"
                                        label="WCS 1"
                                        :suffix="'Z'"
                                        :step="0.01"
                                        :current-pos="wcsOffsets[1][2].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(1, 2)"
                                        @blur="onBlur" />
                                </v-col>
                            </v-row>
                            <v-row dense>
                                <v-col class="col-12 v-subheader text--secondary mr-2">
                                    <span v-if="!el.is.xsmall" class="text-no-wrap">WCS 2</span>
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        :value="wcsOffsets[2][0].toFixed(3)"
                                        label="WCS 2"
                                        :suffix="'X'"
                                        :step="0.01"
                                        :current-pos="wcsOffsets[2][0].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(2, 0)"
                                        @blur="onBlur" />
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        :value="wcsOffsets[2][1].toFixed(3)"
                                        label="WCS 2"
                                        :suffix="'Y'"
                                        :step="0.01"
                                        :current-pos="wcsOffsets[2][1].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(2, 1)"
                                        @blur="onBlur" />
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        :value="wcsOffsets[2][2].toFixed(3)"
                                        label="WCS 2"
                                        :suffix="'Z'"
                                        :step="0.01"
                                        :current-pos="wcsOffsets[2][2].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(2, 2)"
                                        @blur="onBlur" />
                                </v-col>
                            </v-row>
                        </template>
                    </responsive>
                </v-col>
            </v-row>
        </v-container>
    </panel>
</template>

<script lang="ts">
import { Component, Mixins, Watch } from 'vue-property-decorator'
import BaseMixin from '@/components/mixins/base'
import Panel from '@/components/ui/Panel.vue'
import Responsive from '@/components/ui/Responsive.vue'
import WcsInput from '@/components/panels/Module5dControls/WcsInput.vue'
import { mdiChartLineVariant, mdiHome } from '@mdi/js'
import ThemeMixin from '@/components/mixins/theme'
import ControlMixin from '@/components/mixins/control'

@Component({
    components: {
        Panel,
        WcsInput,
        Responsive,
    },
})
export default class WcsGraph extends Mixins(BaseMixin, ControlMixin, ThemeMixin) {
    mdiChartLineVariant = mdiChartLineVariant
    mdiHome = mdiHome
    get strokeColor() {
        return this.themeMode === 'dark' ? '#ffffff' : '#000000'
    }
    get primaryColor(): string {
        return this.$store.state.gui.uiSettings.primary
    }

    get wcsOffsets() {
        return this.$store.state.printer.module_5d.wcs_offsets ?? []
    }

    @Watch('wcsOffsets', { immediate: true, deep: true })
    updateWcsOffsets(newVal: number[][]): void {
        this.offsetsInput = newVal.map((w) => w.map((v) => v.toFixed(3)))
    }

    offsetsInput = [
        ['0', '0', '0'],
        ['0', '0', '0'],
        ['0', '0', '0'],
        ['0', '0', '0'],
        ['0', '0', '0'],
    ]
    aoffsetInput = ''

    get rows() {
        return this.wcsOffsets.map((itm: number[], index: number) => ({
            WCS: `WCS${index}`,
            X: `X ${itm[0].toFixed(3)}`,
            Y: `Y ${itm[1].toFixed(3)}`,
            Z: `Z ${itm[2].toFixed(3)}`,
        }))
    }

    hoveredOffset: { wcs: number; axis: number } = {
        wcs: -1,
        axis: -1,
    }

    onFocus(wcs: number, axis: number) {
        this.hoveredOffset.wcs = wcs
        this.hoveredOffset.axis = axis
    }
    onBlur() {
        this.hoveredOffset.wcs = -1
        this.hoveredOffset.axis = -1
    }

    homePrinter(): void {
        const gcode = 'G28'

        this.$store.dispatch('server/addEvent', { message: gcode, type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: gcode }, { loading: 'homeAll' })
    }

    clearWcs(): void {
        const gcode = 'BED_MESH_CLEAR'

        this.$store.dispatch('server/addEvent', { message: gcode, type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: gcode }, { loading: 'clearWcs' })
    }

    sendCmd() {
        console.log(this.offsetsInput)
    }
}
</script>

<style scoped></style>
