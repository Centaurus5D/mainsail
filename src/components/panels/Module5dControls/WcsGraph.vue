<template>
    <panel :icon="mdiChartLine" :title="$t('Panels.Module5dControlPanel.WcsGraph')" :collapsible="true">
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
                                                    <div v-if="rows[1]" class="text-body2">
                                                        <span
                                                            :style="{
                                                                color:
                                                                    hoveredOffset?.wcs === 1 && hoveredOffset.axis === 0
                                                                        ? 'var(--q-primary)'
                                                                        : strokeColor,
                                                            }">
                                                            {{ rows[1].X }}
                                                        </span>
                                                        <br />
                                                        <span
                                                            :style="{
                                                                color:
                                                                    hoveredOffset?.wcs === 1 && hoveredOffset.axis === 1
                                                                        ? 'var(--q-primary)'
                                                                        : strokeColor,
                                                            }">
                                                            {{ rows[1].Y }}
                                                        </span>
                                                        <br />
                                                        <span
                                                            :style="{
                                                                color:
                                                                    hoveredOffset?.wcs === 1 && hoveredOffset.axis === 2
                                                                        ? 'var(--q-primary)'
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
                                                    <div v-if="rows[2]" class="text-body2">
                                                        <span
                                                            :style="{
                                                                color:
                                                                    hoveredOffset?.wcs === 2 && hoveredOffset.axis === 0
                                                                        ? 'var(--q-primary)'
                                                                        : strokeColor,
                                                            }">
                                                            {{ rows[2].X }}
                                                        </span>
                                                        <br />
                                                        <span
                                                            :style="{
                                                                color:
                                                                    hoveredOffset?.wcs === 2 && hoveredOffset.axis === 1
                                                                        ? 'var(--q-primary)'
                                                                        : strokeColor,
                                                            }">
                                                            {{ rows[2].Y }}
                                                        </span>
                                                        <br />
                                                        <span
                                                            :style="{
                                                                color:
                                                                    hoveredOffset?.wcs === 2 && hoveredOffset.axis === 2
                                                                        ? 'var(--q-primary)'
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
    </panel>
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
