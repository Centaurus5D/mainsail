<template>
    <panel
        :collapsible="true"
        :icon="mdiMoveResize"
        :title="$t('Panels.Module5dControlPanel.ProbeGraph')"
        card-class="probe-graph">
        <v-container>
            <v-row justify="center">
                <v-col cols="12" sm="6" lg="4">
                    <svg
                        v-if="graphVariant === 'MP'"
                        xmlns="http://www.w3.org/2000/svg"
                        style="background: transparent; background-color: transparent; color-scheme: light"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        version="1.1"
                        width="100%"
                        height="100%"
                        viewBox="-0.5 -0.5 218 213">
                        <defs />
                        <g>
                            <g data-cell-id="0">
                                <g data-cell-id="1">
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-11">
                                        <g />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-9">
                                            <g>
                                                <path
                                                    d="M 119 98 L 119 71 Q 119 68 121.68 69.34 L 176.32 96.66 Q 179 98 176.32 99.34 L 121.68 126.66 Q 119 128 119 125 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(90,149,98)"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-7">
                                            <g>
                                                <path
                                                    d="M 119 54.9 C 119 51.09 132.43 48 149 48 C 156.96 48 164.59 48.73 170.21 50.02 C 175.84 51.32 179 53.07 179 54.9 L 179 75.1 C 179 78.91 165.57 82 149 82 C 132.43 82 119 78.91 119 75.1 Z"
                                                    :fill="fillColor"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 179 54.9 C 179 58.72 165.57 61.81 149 61.81 C 132.43 61.81 119 58.72 119 54.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-12">
                                        <g />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-2">
                                            <g>
                                                <path
                                                    d="M 0 6.9 C 0 3.09 7 0 15.63 0 C 19.78 0 23.76 0.73 26.69 2.02 C 29.62 3.32 31.27 5.07 31.27 6.9 L 31.27 117.1 C 31.27 120.91 24.27 124 15.64 124 C 7 124 0 120.91 0 117.1 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 31.27 6.9 C 31.27 10.72 24.27 13.81 15.64 13.81 C 7 13.81 0 10.72 0 6.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-6">
                                            <g>
                                                <path
                                                    d="M 15.53 147 L 15.64 124"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="stroke" />
                                                <ellipse
                                                    cx="15.52"
                                                    cy="150"
                                                    rx="3"
                                                    ry="3"
                                                    :fill="strokeColor"
                                                    :stroke="strokeColor"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-13">
                                        <g>
                                            <path
                                                d="M 16 150 L 14.92 150.62 L 71 183 L 76.23 186.02 L 149 144"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-18">
                                        <g>
                                            <path
                                                d="M 149 144 L 149 128"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-1">
                                        <g>
                                            <rect
                                                x="152"
                                                y="126"
                                                width="65"
                                                height="21"
                                                rx="0.84"
                                                ry="0.84"
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
                                                                width: 63px;
                                                                height: 1px;
                                                                padding-top: 136px;
                                                                margin-left: 153px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 2
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    Z {{ Math.abs(probeOffsets[2]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-5">
                                        <g>
                                            <path
                                                d="M 38.5 194 L 9.5 194 Q 8 194 8.74 192.7 L 19.26 174.3 Q 20 173 21.5 173 L 79.5 173 Q 81 173 80.26 174.3 L 69.74 192.7 Q 69 194 67.5 194 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="translate(0,183.5)scale(1,-1)translate(0,-183.5)rotate(-210,44.5,183.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(30 44.5 183.5)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 184px;
                                                                margin-left: 9px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 1
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    Y {{ Math.abs(probeOffsets[1]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-6">
                                        <g>
                                            <path
                                                d="M 111.5 188 L 82.5 188 Q 81 188 81.74 186.7 L 92.26 168.3 Q 93 167 94.5 167 L 152.5 167 Q 154 167 153.26 168.3 L 142.74 186.7 Q 142 188 140.5 188 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="rotate(150,117.5,177.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(-30 117.5 177.5)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 178px;
                                                                margin-left: 82px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 0
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    X {{ Math.abs(probeOffsets[0]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                </g>
                            </g>
                        </g>
                    </svg>
                    <svg
                        v-else-if="graphVariant === 'MM'"
                        xmlns="http://www.w3.org/2000/svg"
                        style="background: transparent; background-color: transparent; color-scheme: light"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        version="1.1"
                        width="100%"
                        height="100%"
                        viewBox="-0.5 -0.5 143 230">
                        <defs />
                        <g>
                            <g data-cell-id="0">
                                <g data-cell-id="1">
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-11">
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-9" />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-7" />
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-12">
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-2" />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-6" />
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-13" />
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-18" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-1" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-5" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-6" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-1">
                                        <g />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-2">
                                            <g>
                                                <path
                                                    d="M 61.44 50 L 61.44 23 Q 61.44 20 64.12 21.34 L 118.76 48.66 Q 121.44 50 118.76 51.34 L 64.12 78.66 Q 61.44 80 61.44 77 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(90,91.44,50)"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-3">
                                            <g>
                                                <path
                                                    d="M 61.44 6.9 C 61.44 3.09 74.87 0 91.44 0 C 99.4 0 107.03 0.73 112.65 2.02 C 118.28 3.32 121.44 5.07 121.44 6.9 L 121.44 27.1 C 121.44 30.91 108.01 34 91.44 34 C 74.87 34 61.44 30.91 61.44 27.1 Z"
                                                    :fill="fillColor"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 121.44 6.9 C 121.44 10.72 108.01 13.81 91.44 13.81 C 74.87 13.81 61.44 10.72 61.44 6.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-4">
                                        <g />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-5">
                                            <g>
                                                <path
                                                    d="M 110.3 77.9 C 110.3 74.09 117.3 71 125.93 71 C 130.08 71 134.06 71.73 136.99 73.02 C 139.92 74.32 141.57 76.07 141.57 77.9 L 141.57 188.1 C 141.57 189.93 139.92 191.68 136.99 192.98 C 134.06 194.27 130.08 195 125.93 195 C 121.79 195 117.81 194.27 114.88 192.98 C 111.95 191.68 110.3 189.93 110.3 188.1 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 141.57 77.9 C 141.57 79.74 139.92 81.49 136.99 82.79 C 134.06 84.08 130.08 84.81 125.93 84.81 C 121.79 84.81 117.81 84.08 114.88 82.79 C 111.95 81.49 110.3 79.74 110.3 77.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-6">
                                            <g>
                                                <path
                                                    d="M 125.83 218 L 125.93 195"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="stroke" />
                                                <ellipse
                                                    cx="125.82"
                                                    cy="221"
                                                    rx="3"
                                                    ry="3"
                                                    :fill="strokeColor"
                                                    :stroke="strokeColor"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-7">
                                        <g>
                                            <path
                                                d="M 127.44 221 L 126.25 221.69 L 64.44 186 L 0 148.79 L 91.44 96"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-8">
                                        <g>
                                            <path
                                                d="M 91.44 96 L 91.44 80"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-9">
                                        <g>
                                            <rect
                                                x="21.44"
                                                y="75"
                                                width="65"
                                                height="21"
                                                rx="0.84"
                                                ry="0.84"
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
                                                                width: 63px;
                                                                height: 1px;
                                                                padding-top: 86px;
                                                                margin-left: 22px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 2
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    Z {{ Math.abs(probeOffsets[2]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-10">
                                        <g>
                                            <path
                                                d="M 36.94 200 L 7.94 200 Q 6.44 200 7.18 198.7 L 17.7 180.3 Q 18.44 179 19.94 179 L 77.94 179 Q 79.44 179 78.7 180.3 L 68.18 198.7 Q 67.44 200 65.94 200 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="translate(0,189.5)scale(1,-1)translate(0,-189.5)rotate(-210,42.94,189.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(30 42.940000000000055 189.5)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 190px;
                                                                margin-left: 7px;
                                                            ">
                                                            <div
                                                                style="
                                                                    box-sizing: border-box;
                                                                    font-size: 0;
                                                                    text-align: center;
                                                                    color: #000000;
                                                                ">
                                                                <div>
                                                                    <div
                                                                        class="text-caption"
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset === 1
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        Y {{ Math.abs(probeOffsets[1]) }}
                                                                    </div>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-11">
                                        <g>
                                            <path
                                                d="M 53.94 140 L 24.94 140 Q 23.44 140 24.18 138.7 L 34.7 120.3 Q 35.44 119 36.94 119 L 94.94 119 Q 96.44 119 95.7 120.3 L 85.18 138.7 Q 84.44 140 82.94 140 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="rotate(150,59.94,129.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(-30 59.940000000000055 129.5)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 130px;
                                                                margin-left: 24px;
                                                            ">
                                                            <div
                                                                style="
                                                                    box-sizing: border-box;
                                                                    font-size: 0;
                                                                    text-align: center;
                                                                    color: #000000;
                                                                ">
                                                                <div
                                                                    style="
                                                                        display: inline-block;
                                                                        font-size: 12px;
                                                                        font-family: Helvetica;
                                                                        color: #000000;
                                                                        line-height: 1.2;
                                                                        pointer-events: all;
                                                                        white-space: normal;
                                                                        word-wrap: normal;
                                                                    ">
                                                                    <div>
                                                                        <div
                                                                            class="text-caption"
                                                                            :style="{
                                                                                color:
                                                                                    hoveredOffset === 0
                                                                                        ? primaryColor
                                                                                        : strokeColor,
                                                                            }">
                                                                            X {{ Math.abs(probeOffsets[0]) }}
                                                                        </div>
                                                                    </div>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-12">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-13" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-14" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-15">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-16" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-17" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-18" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-19" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-20" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-21" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-22" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-23">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-24" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-25" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-26">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-27" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-28" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-29" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-30" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-31" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-32" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-33" />
                                </g>
                            </g>
                        </g>
                    </svg>
                    <svg
                        v-else-if="graphVariant === 'PM'"
                        xmlns="http://www.w3.org/2000/svg"
                        style="background: transparent; background-color: transparent; color-scheme: light"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        version="1.1"
                        width="100%"
                        height="100%"
                        viewBox="-0.5 -0.5 230 171">
                        <defs />
                        <g>
                            <g data-cell-id="0">
                                <g data-cell-id="1">
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-11">
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-9" />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-7" />
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-12">
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-2" />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-6" />
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-13" />
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-18" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-1" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-5" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-6" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-1">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-2" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-3" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-4">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-5" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-6" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-7" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-8" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-9" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-10" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-11" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-12">
                                        <g />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-13">
                                            <g>
                                                <path
                                                    d="M 38.44 99 L 38.44 72 Q 38.44 69 41.12 70.34 L 95.76 97.66 Q 98.44 99 95.76 100.34 L 41.12 127.66 Q 38.44 129 38.44 126 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(90,68.44,99)"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-14">
                                            <g>
                                                <path
                                                    d="M 38.44 55.9 C 38.44 52.09 51.87 49 68.44 49 C 76.4 49 84.03 49.73 89.65 51.02 C 95.28 52.32 98.44 54.07 98.44 55.9 L 98.44 76.1 C 98.44 79.91 85.01 83 68.44 83 C 51.87 83 38.44 79.91 38.44 76.1 Z"
                                                    :fill="fillColor"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 98.44 55.9 C 98.44 59.72 85.01 62.81 68.44 62.81 C 51.87 62.81 38.44 59.72 38.44 55.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-15">
                                        <g />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-16">
                                            <g>
                                                <path
                                                    d="M 198 6.9 C 198 3.09 205 0 213.63 0 C 217.78 0 221.76 0.73 224.69 2.02 C 227.62 3.32 229.27 5.07 229.27 6.9 L 229.27 117.1 C 229.27 118.93 227.62 120.68 224.69 121.98 C 221.76 123.27 217.78 124 213.63 124 C 209.49 124 205.51 123.27 202.58 121.98 C 199.65 120.68 198 118.93 198 117.1 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 229.27 6.9 C 229.27 8.74 227.62 10.49 224.69 11.79 C 221.76 13.08 217.78 13.81 213.63 13.81 C 209.49 13.81 205.51 13.08 202.58 11.79 C 199.65 10.49 198 8.74 198 6.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-17">
                                            <g>
                                                <path
                                                    d="M 213.53 147 L 213.63 124"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="stroke" />
                                                <ellipse
                                                    cx="213.52"
                                                    cy="150"
                                                    rx="3"
                                                    ry="3"
                                                    :fill="strokeColor"
                                                    :stroke="strokeColor"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-18">
                                        <g>
                                            <path
                                                d="M 216 152 L 177 130 L 135.71 106.16 L 68.44 145"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-19">
                                        <g>
                                            <path
                                                d="M 68.44 145 L 68.44 129"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-20">
                                        <g>
                                            <rect
                                                x="0.44"
                                                y="128"
                                                width="65"
                                                height="21"
                                                rx="0.84"
                                                ry="0.84"
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
                                                                width: 63px;
                                                                height: 1px;
                                                                padding-top: 139px;
                                                                margin-left: 1px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 2
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    Z {{ Math.abs(probeOffsets[2]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-21">
                                        <g>
                                            <path
                                                d="M 164.5 152 L 135.5 152 Q 134 152 134.74 150.7 L 145.26 132.3 Q 146 131 147.5 131 L 205.5 131 Q 207 131 206.26 132.3 L 195.74 150.7 Q 195 152 193.5 152 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="translate(0,141.5)scale(1,-1)translate(0,-141.5)rotate(-210,170.5,141.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(30 170.49992723813193 141.5)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 142px;
                                                                margin-left: 135px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 1
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    Y {{ Math.abs(probeOffsets[1]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-22">
                                        <g>
                                            <path
                                                d="M 101.5 148 L 72.5 148 Q 71 148 71.74 146.7 L 82.26 128.3 Q 83 127 84.5 127 L 142.5 127 Q 144 127 143.26 128.3 L 132.74 146.7 Q 132 148 130.5 148 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="rotate(150,107.5,137.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(-30 107.49992723813193 137.5)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 138px;
                                                                margin-left: 72px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 0
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    X {{ Math.abs(probeOffsets[0]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-23">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-24" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-25" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-26">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-27" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-28" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-29" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-30" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-31" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-32" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-33" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-34" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-35" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-36" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-37" />
                                </g>
                            </g>
                        </g>
                    </svg>
                    <svg
                        v-else-if="graphVariant === 'PP'"
                        xmlns="http://www.w3.org/2000/svg"
                        style="background: transparent; background-color: transparent; color-scheme: light"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        version="1.1"
                        width="100%"
                        height="100%"
                        viewBox="-0.5 -0.5 177 259">
                        <defs />
                        <g>
                            <g data-cell-id="0">
                                <g data-cell-id="1">
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-11">
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-9" />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-7" />
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-12">
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-2" />
                                        <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-6" />
                                    </g>
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-13" />
                                    <g data-cell-id="x2Z6ytbvDR6ljkXhsC0b-18" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-1" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-5" />
                                    <g data-cell-id="w8pLBlEPtyPBULmZi4S8-6" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-1">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-2" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-3" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-4">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-5" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-6" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-7" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-8" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-9" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-10" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-11" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-12">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-13" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-14" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-15">
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-16" />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-17" />
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-18" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-19" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-20" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-21" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-22" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-23">
                                        <g />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-24">
                                            <g>
                                                <path
                                                    d="M 38 193 L 38 166 Q 38 163 40.68 164.34 L 95.32 191.66 Q 98 193 95.32 194.34 L 40.68 221.66 Q 38 223 38 220 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(90,68,193)"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-25">
                                            <g>
                                                <path
                                                    d="M 38 149.9 C 38 146.09 51.43 143 68 143 C 75.96 143 83.59 143.73 89.21 145.02 C 94.84 146.32 98 148.07 98 149.9 L 98 170.1 C 98 173.91 84.57 177 68 177 C 51.43 177 38 173.91 38 170.1 Z"
                                                    :fill="fillColor"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 98 149.9 C 98 153.72 84.57 156.81 68 156.81 C 51.43 156.81 38 153.72 38 149.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-26">
                                        <g />
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-27">
                                            <g>
                                                <path
                                                    d="M 89.87 6.9 C 89.87 3.09 96.87 0 105.5 0 C 109.65 0 113.63 0.73 116.56 2.02 C 119.49 3.32 121.14 5.07 121.14 6.9 L 121.14 117.1 C 121.14 118.93 119.49 120.68 116.56 121.98 C 113.63 123.27 109.65 124 105.5 124 C 101.36 124 97.38 123.27 94.45 121.98 C 91.52 120.68 89.87 118.93 89.87 117.1 Z"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 121.14 6.9 C 121.14 8.74 119.49 10.49 116.56 11.79 C 113.63 13.08 109.65 13.81 105.5 13.81 C 101.36 13.81 97.38 13.08 94.45 11.79 C 91.52 10.49 89.87 8.74 89.87 6.9"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                        <g data-cell-id="LDqJrmm13iMSVyFPym8U-28">
                                            <g>
                                                <path
                                                    d="M 105.4 147 L 105.5 124"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-miterlimit="10"
                                                    pointer-events="stroke" />
                                                <ellipse
                                                    cx="105.39"
                                                    cy="150"
                                                    rx="3"
                                                    ry="3"
                                                    :fill="strokeColor"
                                                    :stroke="strokeColor"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-29">
                                        <g>
                                            <path
                                                d="M 105 150 L 136 169 L 162.62 184.37 L 68 239"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-30">
                                        <g>
                                            <path
                                                d="M 68 239 L 68 223"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="3 3"
                                                pointer-events="stroke" />
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-31">
                                        <g>
                                            <rect
                                                x="0"
                                                y="222"
                                                width="65"
                                                height="21"
                                                rx="0.84"
                                                ry="0.84"
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
                                                                width: 63px;
                                                                height: 1px;
                                                                padding-top: 233px;
                                                                margin-left: 1px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 2
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    Z {{ Math.abs(probeOffsets[2]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-32">
                                        <g>
                                            <path
                                                d="M 132.5 166 L 103.5 166 Q 102 166 102.74 164.7 L 113.26 146.3 Q 114 145 115.5 145 L 173.5 145 Q 175 145 174.26 146.3 L 163.74 164.7 Q 163 166 161.5 166 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="translate(0,155.5)scale(1,-1)translate(0,-155.5)rotate(-210,138.5,155.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(30 138.49992723813193 155.5)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 156px;
                                                                margin-left: 103px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 1
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    Y {{ Math.abs(probeOffsets[1]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-33">
                                        <g>
                                            <path
                                                d="M 104.06 240 L 75.06 240 Q 73.56 240 74.3 238.7 L 84.82 220.3 Q 85.56 219 87.06 219 L 145.06 219 Q 146.56 219 145.82 220.3 L 135.3 238.7 Q 134.56 240 133.06 240 Z"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-miterlimit="10"
                                                transform="rotate(150,110.06,229.5)"
                                                pointer-events="all" />
                                        </g>
                                        <g>
                                            <g transform="rotate(-30 110.05992723813188 229.50000000000023)">
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
                                                                width: 71px;
                                                                height: 1px;
                                                                padding-top: 230px;
                                                                margin-left: 75px;
                                                            ">
                                                            <div>
                                                                <div
                                                                    class="text-caption"
                                                                    :style="{
                                                                        color:
                                                                            hoveredOffset === 0
                                                                                ? primaryColor
                                                                                : strokeColor,
                                                                    }">
                                                                    X {{ Math.abs(probeOffsets[0]) }}
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-34" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-35" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-36" />
                                    <g data-cell-id="LDqJrmm13iMSVyFPym8U-37" />
                                </g>
                            </g>
                        </g>
                    </svg>
                </v-col>
                <v-col cols="12" sm="8" lg="6">
                    <responsive
                        :breakpoints="{
                            xsmall: (el) => el.width <= 320,
                            small: (el) => el.width > 320 && el.width <= 460,
                            medium: (el) => el.width > 460 && el.width <= 560,
                            large: (el) => el.width > 560,
                        }">
                        <template #default="{ el }">
                            <v-row dense>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        v-model="offsetsInput[0]"
                                        label="Offset"
                                        :suffix="'X'"
                                        :step="0.01"
                                        :current-pos="probeOffsets[0].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(0)"
                                        @blur="onBlur" />
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        v-model="offsetsInput[1]"
                                        label="Offset"
                                        :suffix="'Y'"
                                        :step="0.01"
                                        :current-pos="probeOffsets[1].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(1)"
                                        @blur="onBlur" />
                                </v-col>
                                <v-col :class="el.is.xsmall ? 'col-12' : 'col-4'">
                                    <wcs-input
                                        v-model="offsetsInput[2]"
                                        label="Offset"
                                        :suffix="'Z'"
                                        :step="0.01"
                                        :current-pos="probeOffsets[2].toFixed(3)"
                                        @submit="sendCmd"
                                        @focus="onFocus(2)"
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
import { mdiMoveResize } from '@mdi/js'
import ThemeMixin from '@/components/mixins/theme'
import ControlMixin from '@/components/mixins/control'

type GraphVariant = 'MM' | 'PM' | 'MP' | 'PP'

@Component({
    components: {
        Panel,
        WcsInput,
        Responsive,
    },
})
export default class ProbeGraph extends Mixins(BaseMixin, ControlMixin, ThemeMixin) {
    mdiMoveResize = mdiMoveResize

    get graphVariant() {
        const res: string[] = []
        res.push(this.probeOffsets[0] < 0 ? 'M' : 'P')
        res.push(this.probeOffsets[1] < 0 ? 'M' : 'P')
        return res.join('') as GraphVariant
    }

    get strokeColor() {
        return this.themeMode === 'dark' ? '#ffffff' : '#000000'
    }
    get fillColor() {
        return this.themeMode === 'dark' ? '#1E1E1E' : '#ffffff'
    }

    get primaryColor(): string {
        return this.$store.state.gui.uiSettings.primary
    }

    get probeOffsets() {
        return this.$store.state.printer.module_5d_probe.offsets ?? []
    }

    @Watch('probeOffsets', { immediate: true, deep: true })
    updateOffsets(newVal: number[]): void {
        this.offsetsInput = newVal.map((v) => v.toFixed(3))
    }

    offsetsInput = ['0', '0', '0']

    get rows() {
        return this.wcsOffsets.map((itm: number[], index: number) => ({
            WCS: index,
            X: itm[0].toFixed(3),
            Y: itm[1].toFixed(3),
            Z: itm[2].toFixed(3),
        }))
    }

    hoveredOffset: number = -1

    onFocus(axis: number) {
        this.hoveredOffset = axis
    }
    onBlur() {
        this.hoveredOffset = -1
    }

    homePrinter(): void {
        const gcode = 'G28'

        this.$store.dispatch('server/addEvent', { message: gcode, type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: gcode }, { loading: 'homeAll' })
    }

    clearWcs(): void {
        const gcode = 'CLEAR_WCS'

        this.$store.dispatch('server/addEvent', { message: gcode, type: 'command' })
        this.$socket.emit('printer.gcode.script', { script: gcode }, { loading: 'clearWcs' })
    }

    sendCmd() {
        for (let wcs_index = 1; wcs_index < 3; wcs_index++) {
            const wcs = this.offsetsInput[wcs_index]
            let command = `G10 L2 P${wcs_index + 1}`
            if (wcs[0] !== this.rows[wcs_index].X) command += ` X${wcs[0]}`
            if (wcs[1] !== this.rows[wcs_index].Y) command += ` Y${wcs[1]}`
            if (wcs[2] !== this.rows[wcs_index].Z) command += ` Z${wcs[2]}`
            this.$store.dispatch('server/addEvent', { message: command, type: 'command' })
            this.$socket.emit('printer.gcode.script', { script: command })
        }
    }

    sendOffset() {
        if (this.aoffsetInput !== this.homingOffsets[0].toFixed(3)) {
            const gcode = `SET_GCODE_OFFSET A=${this.aoffsetInput}`
            this.$store.dispatch('server/addEvent', { message: gcode, type: 'command' })
            this.$socket.emit('printer.gcode.script', { script: gcode })
        }
    }
}
</script>

<style scoped></style>
