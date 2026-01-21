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
                {{ $t('Heightmap.Clear') }}
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
                        viewBox="0 0 1098 1133">
                        <defs />
                        <g>
                            <g data-cell-id="0">
                                <g data-cell-id="1">
                                    <g data-cell-id="y3XOAQ3aAnnzej_5DS3p-7" />
                                    <g data-cell-id="y3XOAQ3aAnnzej_5DS3p-5">
                                        <g>
                                            <g>
                                                <svg
                                                    id="svg565"
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    version="1.1"
                                                    width="100%"
                                                    height="100%"
                                                    viewBox="0 0 730.53101 754.28967"
                                                    x="-1"
                                                    y="0"
                                                    style="font-family: initial">
                                                    &#xa;
                                                    <defs id="defs2" />
                                                    &#xa;
                                                    <g id="g567" transform="translate(-158.80405,223.04544)">
                                                        &#xa;
                                                        <path
                                                            id="path62"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 647.49,437.73 -3.84,-0.36 -3.63,0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path63"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 637.32,441.63 2.76,0.33" />
                                                        &#xa;
                                                        <path
                                                            id="path64"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.5,490.8 2.19,-2.88 1.62,-3.51" />
                                                        &#xa;
                                                        <path
                                                            id="path65"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 666.9,488.67 -1.11,2.55" />
                                                        &#xa;
                                                        <path
                                                            id="path81"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 676.08,464.25 -0.33,0.54" />
                                                        &#xa;
                                                        <path
                                                            id="path82"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 665.16,452.4 0.48,-0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path83"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 665.64,452.25 1.08,3.3 1.74,3.06 2.28,2.64 2.61,1.92 2.73,1.08" />
                                                        &#xa;
                                                        <path
                                                            id="path84"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 672.36,441.78 -2.49,0.24 -2.1,1.14 -1.53,2.01 -0.78,2.67 -0.03,3.12" />
                                                        &#xa;
                                                        <path
                                                            id="path85"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 664.92,451.08 0.51,-0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path86"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 683.85,453.96 -1.05,-3.3 -1.74,-3.06 -2.28,-2.64 -2.61,-1.92 -2.73,-1.08" />
                                                        &#xa;
                                                        <path
                                                            id="path87"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 677.13,464.43 676.8,465" />
                                                        &#xa;
                                                        <path
                                                            id="path88"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 677.13,464.43 2.52,-0.24 2.1,-1.14 1.5,-2.01 0.81,-2.67 0.03,-3.12" />
                                                        &#xa;
                                                        <path
                                                            id="path93"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.44,441.96 -1.98,-0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path94"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 683.73,459.87 -0.6,1.92" />
                                                        &#xa;
                                                        <path
                                                            id="path95"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.53,431.55 0.06,0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path96"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.38,431.46 0.03,0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path97"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 654.99,434.67 -0.12,0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path98"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 654.87,434.82 -8.64,4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path99"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 646.29,439.65 v 0.03 l -0.06,0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path100"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 644.91,462.66 0.06,0.12 0.03,0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path101"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 644.91,462.66 8.67,-4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path102"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 653.58,457.68 0.09,0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path103"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 653.67,457.95 645,462.9" />
                                                        &#xa;
                                                        <path
                                                            id="path104"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.74,477.6 0.24,0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path105"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.98,477.72 -8.67,4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path106"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.07,482.58 0.15,0.06 0.09,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path107"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.07,482.58 8.67,-4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path108"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 689.46,474.36 -0.12,0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path109"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 680.67,479.49 h 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path110"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 680.67,479.49 8.67,-4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path111"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 690.78,451.5 v 0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path112"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 690.63,451.14 0.15,0.45" />
                                                        &#xa;
                                                        <path
                                                            id="path113"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 690.63,451.14 0.03,0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path114"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 653.61,457.56 -0.03,0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path115"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 653.61,457.56 0.18,0.45" />
                                                        &#xa;
                                                        <path
                                                            id="path116"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 653.67,457.95 0.12,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path117"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 667.92,434.73 3.36,-0.03 3.54,0.93 3.54,1.89 3.33,2.7 2.97,3.42 2.43,3.93 1.77,4.23 0.99,4.29 0.21,4.14 -0.66,3.75 -1.41,3.18 -2.16,2.4 -2.73,1.53 -3.21,0.57 -3.45,-0.45 -3.57,-1.44 -3.48,-2.31 -3.15,-3.09 -2.73,-3.69 -2.1,-4.11 -1.41,-4.29 -0.6,-4.26 0.24,-3.96 1.02,-3.48 1.8,-2.82 2.46,-1.98 3,-1.05" />
                                                        &#xa;
                                                        <path
                                                            id="path118"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.32,431.46 -1.89,0.12 -1.92,0.15 -4.02,0.57 -4.62,0.93 -2.67,0.63 -3.09,0.78" />
                                                        &#xa;
                                                        <path
                                                            id="path119"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.32,431.46 0.39,0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path120"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.71,431.64 2.88,2.34 2.55,2.25 4.29,4.44 3.72,4.77 1.74,2.7 1.74,3" />
                                                        &#xa;
                                                        <path
                                                            id="path121"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 690.78,451.59 0.42,2.76 0.24,2.64 -0.03,5.19 -0.6,5.55 -0.54,3.09 -0.78,3.42" />
                                                        &#xa;
                                                        <path
                                                            id="path122"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 689.49,474.24 -0.21,0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path123"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 689.28,474.51 -1.89,0.12 -1.92,0.15 -4.02,0.6 -4.62,0.9 -2.67,0.63 -3.09,0.78" />
                                                        &#xa;
                                                        <path
                                                            id="path124"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.71,477.51 0.36,0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path125"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.71,477.51 -1.74,-3 -1.74,-2.7 -3.72,-4.8 -4.29,-4.44 -2.55,-2.22 -2.88,-2.34" />
                                                        &#xa;
                                                        <path
                                                            id="path126"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 653.61,457.56 0.75,-3.42 0.57,-3.12 0.6,-5.52 v -5.19 l -0.21,-2.64 -0.42,-2.76" />
                                                        &#xa;
                                                        <path
                                                            id="path127"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 655.11,434.64 -0.21,0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path128"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 683.82,454.02 0.24,1.23" />
                                                        &#xa;
                                                        <path
                                                            id="path129"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 684.15,456.27 -0.09,2.58 -0.6,2.28 -1.11,1.86 -1.53,1.35" />
                                                        &#xa;
                                                        <path
                                                            id="path130"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 668.1,442.2 1.95,-0.66 h 2.16 l 2.28,0.63 2.25,1.2" />
                                                        &#xa;
                                                        <path
                                                            id="path131"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 672.9,441.69 2.34,0.87" />
                                                        &#xa;
                                                        <path
                                                            id="path132"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 683.79,454.14 0.18,1.11" />
                                                        &#xa;
                                                        <path
                                                            id="path133"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 684.12,458.01 -0.45,2.46" />
                                                        &#xa;
                                                        <path
                                                            id="path134"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.97,490.89 0.84,-0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path135"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 636.18,444.24 0.78,-0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path136"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 651.54,436.11 0.93,-0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path137"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 640.53,450.69 0.9,-3.84 1.92,-3.69 2.88,-3.51 0.93,-1.53 1.8,-1.2 2.58,-0.81" />
                                                        &#xa;
                                                        <path
                                                            id="path138"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 640.53,450.69 -0.06,1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path139"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 649.29,475.62 -2.34,-3.75 -1.47,-4.32 -0.57,-4.77 -2.49,-3.45 -1.5,-3.69 -0.45,-3.81" />
                                                        &#xa;
                                                        <path
                                                            id="path140"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 649.29,475.62 0.84,0.96" />
                                                        &#xa;
                                                        <path
                                                            id="path141"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 669.96,485.82 -2.91,-0.09 -2.64,-1.05 -2.22,-1.98 -4.62,-1.2 -4.05,-2.07 -3.39,-2.85" />
                                                        &#xa;
                                                        <path
                                                            id="path142"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 669.96,485.82 0.93,-0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path143"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 680.79,479.49 -3.36,2.94 -3.33,2.07 -3.21,1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path144"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 680.79,479.43 v 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path145"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 652.47,435.96 0.33,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path146"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 661.11,455.46 -1.2,-4.26 -0.39,-4.17 0.42,-3.84 1.23,-3.3 1.98,-2.61 2.58,-1.74 3.06,-0.78 3.39,0.18 3.54,1.17 3.48,2.1 3.24,2.88 2.85,3.54 2.25,3.99 1.56,4.26 0.81,4.23 -0.03,4.05 -0.84,3.6 -1.59,2.97 -2.31,2.16 -2.85,1.29 -3.24,0.3 -3.48,-0.69 -3.54,-1.65 -3.39,-2.49 -3.06,-3.24 -2.55,-3.78 -1.92,-4.17" />
                                                        &#xa;
                                                        <path
                                                            id="path147"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 665.76,454.68 -0.9,-3.48 -0.09,-3.3 0.72,-2.88 1.47,-2.22 2.1,-1.38 2.55,-0.45 2.82,0.54 2.85,1.47 2.64,2.31 2.22,2.91 1.62,3.33 0.9,3.48 0.09,3.3 -0.72,2.88 -1.47,2.22 -2.1,1.38 -2.58,0.45 -2.82,-0.54 -2.82,-1.47 -2.64,-2.31 -2.22,-2.91 -1.62,-3.33" />
                                                        &#xa;
                                                        <path
                                                            id="path148"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 668.22,442.14 2.37,-0.75 2.7,0.18 2.79,1.14 2.7,1.98 2.31,2.67 1.83,3.15 1.11,3.36 0.39,3.33 -0.45,2.97 -1.17,2.43 -1.86,1.68" />
                                                        &#xa;
                                                        <path
                                                            id="path149"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 651.54,436.11 0.93,-0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path150"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 646.29,439.68 -0.06,-0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path151"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 640.47,451.83 0.06,-1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path152"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 646.23,439.8 -1.32,22.86" />
                                                        &#xa;
                                                        <path
                                                            id="path153"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 644.97,462.78 h -0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path154"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 680.79,479.43 v 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path155"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.89,485.64 -0.93,0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path156"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.22,482.64 -0.03,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path157"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.31,482.7 18.36,-3.21" />
                                                        &#xa;
                                                        <path
                                                            id="path158"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 650.13,476.58 -0.84,-0.96" />
                                                        &#xa;
                                                        <path
                                                            id="path159"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 645,462.9 17.07,19.68" />
                                                        &#xa;
                                                        <path
                                                            id="path160"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 689.49,474.24 -0.03,0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path161"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.98,477.72 0.09,-0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path162"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 689.28,474.51 h 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path163"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 670.71,477.51 0.03,0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path164"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 654.87,434.82 0.03,0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path165"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.32,431.46 h 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path166"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 654.99,434.67 0.12,-0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path167"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.59,431.58 0.12,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path168"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 654.93,434.7 -8.64,4.95" />
                                                        &#xa;
                                                        <path
                                                            id="path169"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 689.37,474.51 -8.64,4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path170"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 690.66,451.23 0.12,0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path171"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 668.1,442.2 2.25,-0.69 2.55,0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path172"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 683.67,460.47 -1.14,2.28 -1.71,1.59" />
                                                        &#xa;
                                                        <path
                                                            id="path173"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 663,490.89 0.81,-0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path174"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 636.18,444.24 0.78,-0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path175"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 663.81,490.47 11.31,-6.51" />
                                                        &#xa;
                                                        <path
                                                            id="path176"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 636.96,443.76 11.34,-6.51" />
                                                        &#xa;
                                                        <path
                                                            id="path177"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 680.94,464.28 -1.56,0.6 -1.74,0.18 -1.86,-0.27 -1.92,-0.72 -1.89,-1.14 -1.8,-1.53 -1.62,-1.83 -1.41,-2.1 -1.08,-2.25 -0.78,-2.34 -0.42,-2.31 -0.03,-2.22 0.36,-2.01 0.69,-1.77 1.02,-1.41 1.32,-1.02" />
                                                        &#xa;
                                                        <path
                                                            id="path178"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 673.41,431.49 0.12,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path232"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 405.78,473.13 5.88,-3.87 5.82,-4.71 5.67,-5.49 5.46,-6.21 5.19,-6.84 4.86,-7.38 4.47,-7.89 4.05,-8.25 3.54,-8.55 3,-8.7 2.43,-8.82 1.83,-8.76" />
                                                        &#xa;
                                                        <path
                                                            id="path234"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 458.13,349.38 -0.96,-3.99 -1.2,-3.81" />
                                                        &#xa;
                                                        <path
                                                            id="path235"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 457.98,387.66 0.15,-38.28" />
                                                        &#xa;
                                                        <path
                                                            id="path246"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 494.94,508.5 h 0.72" />
                                                        &#xa;
                                                        <path
                                                            id="path247"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 741.69,598.95 502.41,503.97" />
                                                        &#xa;
                                                        <path
                                                            id="path248"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 746.04,605.67 -0.33,-2.04 -0.93,-2.01 -1.41,-1.62 -1.68,-1.05" />
                                                        &#xa;
                                                        <path
                                                            id="path249"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 746.04,606.9 v -1.23" />
                                                        &#xa;
                                                        <path
                                                            id="path250"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 747.12,608.58 -0.75,-0.66 -0.33,-1.02" />
                                                        &#xa;
                                                        <path
                                                            id="path251"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 888.48,558.48 -1.83,8.79 -2.43,8.79 -3.03,8.73 -3.51,8.52 -4.05,8.28 -4.47,7.86 -4.86,7.41 -5.19,6.84 -5.46,6.21 -5.67,5.46 -5.82,4.71 -5.88,3.87" />
                                                        &#xa;
                                                        <path
                                                            id="path252"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 888.63,520.2 -0.15,38.28" />
                                                        &#xa;
                                                        <path
                                                            id="path253"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 867.57,490.38 4.26,2.16 3.87,2.88 3.51,3.66 3.06,4.35 2.61,5.01 2.13,5.61 1.62,6.15" />
                                                        &#xa;
                                                        <path
                                                            id="path254"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 888.63,520.2 807.78,488.13" />
                                                        &#xa;
                                                        <path
                                                            id="path255"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 784.2,462.99 -84,-33.33" />
                                                        &#xa;
                                                        <path
                                                            id="path256"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 631.2,402.3 -84,-33.36" />
                                                        &#xa;
                                                        <path
                                                            id="path257"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 538.98,381.48 -80.85,-32.1" />
                                                        &#xa;
                                                        <path
                                                            id="path258"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 807.63,526.41 80.85,32.07" />
                                                        &#xa;
                                                        <path
                                                            id="path259"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 457.98,387.66 80.88,32.07" />
                                                        &#xa;
                                                        <path
                                                            id="path260"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 546.9,453.78 84,33.36" />
                                                        &#xa;
                                                        <path
                                                            id="path261"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 699.87,514.5 84.03,33.33" />
                                                        &#xa;
                                                        <path
                                                            id="path262"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 795.57,472.59 2.64,3.87 2.7,3.96 1.47,2.1 1.59,2.16 1.77,1.98 0.99,0.87 1.05,0.6" />
                                                        &#xa;
                                                        <path
                                                            id="path263"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 538.98,381.48 0.96,0.18 0.78,-0.15 1.08,-0.87 0.75,-1.23 0.48,-1.32 0.42,-2.73 -0.21,-2.91" />
                                                        &#xa;
                                                        <path
                                                            id="path565"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 434.88606,530.53929 4.26,-2.16 3.87,-2.88 3.51,-3.66 3.06,-4.35 2.61,-5.01 2.13,-5.61 1.62,-6.15" />
                                                        &#xa;
                                                        <path
                                                            id="path264"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 807.78,488.13 -0.15,38.28" />
                                                        &#xa;
                                                        <path
                                                            id="path265"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 543,439.92 0.24,-5.52 -0.39,-5.31 -0.48,-2.67 -0.72,-2.67 -1.08,-2.37 -0.78,-0.99 -0.93,-0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path266"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 807.63,526.41 -1.02,-0.15 -1.02,0.3 -1.77,1.23 -1.62,1.74 -1.5,1.89 -2.7,4.05 -2.67,4.56" />
                                                        &#xa;
                                                        <path
                                                            id="path267"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 538.86,419.73 0.12,-38.25" />
                                                        &#xa;
                                                        <path
                                                            id="path268"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 543.45,374.85 -0.21,60.51" />
                                                        &#xa;
                                                        <path
                                                            id="path269"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 784.2,462.99 1.65,0.78 1.77,1.05 1.65,1.14 1.53,1.26 2.73,2.73 2.04,2.64" />
                                                        &#xa;
                                                        <path
                                                            id="path270"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 543.24,372.45 -0.18,-1.89 0.36,-1.5 0.48,-0.45 0.75,-0.21 1.11,0.09 1.44,0.45" />
                                                        &#xa;
                                                        <path
                                                            id="path271"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 546.9,453.78 -1.44,-0.9 -1.11,-1.41 -0.75,-1.65 -0.48,-1.89 -0.33,-4.08 0.21,-3.93" />
                                                        &#xa;
                                                        <path
                                                            id="path272"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 795.33,540.03 -2.07,3.21 -2.73,2.88 -1.56,1.05 -1.65,0.72 -1.77,0.27 -1.65,-0.33" />
                                                        &#xa;
                                                        <path
                                                            id="path273"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 795.57,472.59 -0.24,67.44" />
                                                        &#xa;
                                                        <path
                                                            id="path274"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 783.9,547.83 0.3,-84.84" />
                                                        &#xa;
                                                        <path
                                                            id="path275"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 547.2,368.94 -0.3,84.84" />
                                                        &#xa;
                                                        <path
                                                            id="path276"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 687.09,420.78 1.77,0.84 1.86,1.05 1.56,1.11 1.35,1.14 1.41,1.23 1.56,1.26 1.77,1.29 0.93,0.54 0.9,0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path277"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 631.2,402.3 0.78,0.21 0.57,0.06 0.63,-0.33 0.09,-0.6 -0.33,-0.81 -0.33,-0.72 0.06,-0.45 0.66,-0.09 1.32,0.39" />
                                                        &#xa;
                                                        <path
                                                            id="path278"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 634.26,501.6 -1.32,-1.11 -0.63,-1.74 -0.06,-1.98 0.33,-2.1 0.36,-2.22 -0.09,-2.13 -0.6,-1.95 -0.6,-0.75 -0.75,-0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path279"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 699.87,514.5 -0.87,-0.15 -0.93,0.15 -1.8,0.99 -1.56,1.47 -1.41,1.8 -1.38,1.71 -1.56,1.32 -1.86,0.75 -1.8,-0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path280"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 634.32,490.35 -0.06,11.25" />
                                                        &#xa;
                                                        <path
                                                            id="path281"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 634.59,411.24 -0.39,3.42 -1.11,2.91 -1.8,2.25 -3.48,3.78 -2.76,4.59 -2.04,5.25 -1.23,5.85 -0.45,6.3 0.39,6.63 1.2,6.81 1.98,6.84 2.73,6.75 3.45,6.54 1.77,3.66 1.08,3.81 0.39,3.72" />
                                                        &#xa;
                                                        <path
                                                            id="path282"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 634.65,399.96 -0.06,11.28" />
                                                        &#xa;
                                                        <path
                                                            id="path283"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 687.03,432.06 0.06,-11.28" />
                                                        &#xa;
                                                        <path
                                                            id="path284"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 686.76,511.14 0.39,-3.39 1.11,-2.94 1.8,-2.25 3.48,-3.78 2.76,-4.59 2.04,-5.25 1.23,-5.85 0.45,-6.3 -0.39,-6.6 -1.2,-6.81 -1.98,-6.87 -2.76,-6.75 -3.42,-6.51 -1.77,-3.69 -1.08,-3.78 -0.39,-3.72" />
                                                        &#xa;
                                                        <path
                                                            id="path285"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 686.7,522.42 0.06,-11.28" />
                                                        &#xa;
                                                        <path
                                                            id="path286"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 631.2,405.15 V 402.3" />
                                                        &#xa;
                                                        <path
                                                            id="path287"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 630.93,484.26 -0.33,-2.07 -0.87,-2.07 -2.7,-4.86 -2.37,-5.04 -2.04,-5.13 -1.68,-5.16 -1.29,-5.19 -0.96,-5.16 -0.57,-5.1 -0.18,-4.98 0.21,-4.8 0.6,-4.62 0.99,-4.41 1.35,-4.14 1.71,-3.81 2.07,-3.48 2.4,-3.15 2.7,-2.76 0.9,-1.35 0.33,-1.83" />
                                                        &#xa;
                                                        <path
                                                            id="path288"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 630.9,487.14 0.03,-2.88" />
                                                        &#xa;
                                                        <path
                                                            id="path289"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 700.2,429.66 -0.03,2.88" />
                                                        &#xa;
                                                        <path
                                                            id="path290"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 700.17,432.54 -2.04,-0.54 -2.34,-0.09 -2.19,0.39" />
                                                        &#xa;
                                                        <path
                                                            id="path291"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 693.6,432.3 0.03,-7.38" />
                                                        &#xa;
                                                        <path
                                                            id="path292"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 700.17,432.54 0.33,2.07 0.87,2.04 -1.62,0.99 -1.95,1.17 -1.98,1.14 -0.93,-1.86 -0.72,-1.95 -0.42,-1.95 -0.15,-1.89" />
                                                        &#xa;
                                                        <path
                                                            id="path293"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 701.37,436.65 2.67,4.89 2.4,5.04 2.01,5.13 1.68,5.16 1.32,5.19 0.96,5.16 0.57,5.1 0.18,4.98 -0.21,4.8 -0.6,4.62 -0.99,4.41 -1.35,4.11 -1.71,3.84 -2.07,3.48 -2.4,3.15 -2.7,2.76 -1.62,-1.68 -1.95,-1.05 -1.98,-0.24 2.49,-2.52 2.19,-2.85 1.89,-3.18 1.56,-3.51 1.23,-3.75 0.9,-4.05 0.54,-4.2 0.21,-4.38 -0.18,-4.56 -0.51,-4.65 -0.87,-4.71 -1.2,-4.74 -1.53,-4.71 -1.86,-4.68 -2.16,-4.62 -2.46,-4.44" />
                                                        &#xa;
                                                        <path
                                                            id="path294"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 701.13,508.47 -0.9,1.32 -0.33,1.83 -2.07,-0.51 -2.31,-0.09 -2.19,0.36 0.15,-1.77 0.45,-1.62 0.69,-1.38 0.96,-1.11" />
                                                        &#xa;
                                                        <path
                                                            id="path295"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 693.3,518.76 0.03,-7.38" />
                                                        &#xa;
                                                        <path
                                                            id="path296"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 699.9,511.62 -0.03,2.88" />
                                                        &#xa;
                                                        <path
                                                            id="path297"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 630.93,484.26 1.5,0.93 0.54,1.17" />
                                                        &#xa;
                                                        <path
                                                            id="path298"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 629.73,480.12 0.93,-0.57 0.33,-0.24" />
                                                        &#xa;
                                                        <path
                                                            id="path299"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 629.97,408.33 1.02,2.01 0.24,2.04 -0.6,1.71 -2.49,2.52 -2.19,2.88" />
                                                        &#xa;
                                                        <path
                                                            id="path300"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 631.2,405.15 1.53,0.93 0.54,1.17" />
                                                        &#xa;
                                                        <path
                                                            id="path301"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 631.59,412.95 -0.96,1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path302"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 634.59,411.24 -1.02,-0.51 -0.69,-0.63" />
                                                        &#xa;
                                                        <path
                                                            id="path303"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 631.29,419.82 -1.02,-2.01 -0.24,-2.04 0.6,-1.68" />
                                                        &#xa;
                                                        <path
                                                            id="path304"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 630.93,479.22 0.15,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path305"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 632.97,489.57 1.35,0.78" />
                                                        &#xa;
                                                        <path
                                                            id="path306"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 686.76,511.14 2.04,0.54 2.34,0.09 2.19,-0.39" />
                                                        &#xa;
                                                        <path
                                                            id="path307"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 690.06,502.56 1.62,1.68 1.95,1.05 1.95,0.21" />
                                                        &#xa;
                                                        <path
                                                            id="path308"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 690.27,443.25 1.65,-0.99 1.95,-1.17 1.95,-1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path309"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 687.03,432.06 2.07,0.51 2.31,0.09 2.19,-0.36" />
                                                        &#xa;
                                                        <path
                                                            id="path310"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 632.97,486.36 -0.03,5.4" />
                                                        &#xa;
                                                        <path
                                                            id="path311"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 625.95,419.49 -1.53,2.55 -1.32,2.79 -1.11,3.03 -0.87,3.3 -0.63,3.51 -0.36,3.66 -0.12,3.84 0.15,3.99 0.45,4.08 0.69,4.17 0.99,4.2 1.23,4.23 1.5,4.2 1.77,4.2 1.98,4.08 2.22,3.99 1.44,3.36 0.42,1.8 0.12,1.89" />
                                                        &#xa;
                                                        <path
                                                            id="path312"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 633.27,407.25 -0.39,2.88 -1.29,2.82" />
                                                        &#xa;
                                                        <path
                                                            id="path313"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 633.27,401.85 v 5.4" />
                                                        &#xa;
                                                        <path
                                                            id="path314"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 687.09,420.78 634.65,399.96" />
                                                        &#xa;
                                                        <path
                                                            id="path315"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 634.26,501.6 52.44,20.82" />
                                                        &#xa;
                                                        <path
                                                            id="path328"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 765.15,585.36 0.93,0.72 0.42,1.08 -0.18,2.37 -0.96,2.37 -1.35,2.25 -3.39,4.08 -3.9,3.6 -4.77,3.66 -4.83,3.09" />
                                                        &#xa;
                                                        <path
                                                            id="path329"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 523.89,489.63 241.26,95.73" />
                                                        &#xa;
                                                        <path
                                                            id="path330"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 494.94,508.5 4.83,-3.09 4.77,-3.66 4.08,-3.51 4.41,-3.69 2.4,-1.83 2.64,-1.68 2.88,-1.32 1.53,-0.3 1.41,0.21" />
                                                        &#xa;
                                                        <path
                                                            id="path331"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 746.04,606.9 4.74,-3.03 4.68,-3.6 3.84,-3.27 3.42,-3.66 1.44,-1.98 1.11,-2.07 0.42,-2.07 -0.24,-0.9 -0.72,-0.6" />
                                                        &#xa;
                                                        <path
                                                            id="path332"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 764.73,585.72 523.47,489.96" />
                                                        &#xa;
                                                        <path
                                                            id="path333"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 523.47,489.96 -1.17,-0.12 -1.35,0.3 -2.67,1.26" />
                                                        &#xa;
                                                        <path
                                                            id="path334"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 504.54,501.75 0.72,-0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path335"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 755.46,600.27 0.42,0.9 0.84,0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path336"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 764.73,585.72 0.42,-0.36" />
                                                        &#xa;
                                                        <path
                                                            id="path337"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 523.47,489.96 0.42,-0.33" />
                                                        &#xa;
                                                        <path
                                                            id="path338"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 518.28,491.4 -3.6,2.43 -3.3,2.67 -3.09,2.67 -3.03,2.55 -4.77,3.66 -4.83,3.12" />
                                                        &#xa;
                                                        <path
                                                            id="path351"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 657.03,434.13 -4.23,-0.84 -4.02,0.09 -3.72,0.96 -3.27,1.89 -2.73,2.7 -2.1,3.45 -1.41,4.08 -0.66,4.56 0.09,4.92 0.87,5.13" />
                                                        &#xa;
                                                        <path
                                                            id="path352"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 648.27,482.7 3.93,3.27 4.11,2.55 4.23,1.74 4.14,0.87 h 3.99 l 3.66,-0.9 3.27,-1.74 2.76,-2.55 2.16,-3.3 1.5,-3.9" />
                                                        &#xa;
                                                        <path
                                                            id="path353"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 686.55,476.13 -1.14,4.74 -1.98,4.11 -2.67,3.36 -3.36,2.46 -3.87,1.53 -4.29,0.51 -4.56,-0.48 -4.68,-1.5 -4.68,-2.46 -4.5,-3.33 -4.17,-4.08 -3.75,-4.74 -3.15,-5.22 -2.49,-5.52 -1.74,-5.67 -0.9,-5.61 -0.09,-5.43 0.75,-4.98 1.56,-4.44 2.34,-3.75 3.03,-2.94 3.6,-1.98 4.11,-1.05 h 4.44 l 4.65,0.99 4.71,1.98" />
                                                        &#xa;
                                                        <path
                                                            id="path354"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 679.08,481.11 -1.5,3.51 -2.04,3 -2.55,2.34" />
                                                        &#xa;
                                                        <path
                                                            id="path355"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 642.03,436.05 3.57,-1.05 3.87,-0.21 4.08,0.69" />
                                                        &#xa;
                                                        <path
                                                            id="path357"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 741.69,598.95 23.04,-13.23" />
                                                        &#xa;
                                                        <path
                                                            id="path378"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 867.57,490.38 456.03,327.06" />
                                                        &#xa;
                                                        <path
                                                            id="path426"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 438.27,532.83 778.95,668.01" />
                                                        &#xa;
                                                        <path
                                                            id="path427"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 771.57,668.37 434.22,534.48" />
                                                        &#xa;
                                                        <path
                                                            id="path428"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 778.95,668.01 -2.61,0.78 -2.49,0.12 -2.28,-0.54" />
                                                        &#xa;
                                                        <path
                                                            id="path429"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 829.29,647.43 -50.34,20.58" />
                                                        &#xa;
                                                        <path
                                                            id="path430"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 835.92,644.16 -3.33,1.8 -3.3,1.47" />
                                                        &#xa;
                                                        <path
                                                            id="path457"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 565.44,586.56 -4.83,-1.68 -2.64,-1.02 -2.85,-1.11 -3.03,-1.2 -3.15,-1.29 -6.51,-2.85" />
                                                        &#xa;
                                                        <path
                                                            id="path458"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 385.05,554.61 53.22,-21.78" />
                                                        &#xa;
                                                        <path
                                                            id="path459"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 377.67,554.94 2.28,0.54 2.49,-0.12 2.61,-0.75" />
                                                        &#xa;
                                                        <path
                                                            id="path467"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 295.23,518.97 398.79,476.58" />
                                                        &#xa;
                                                        <path
                                                            id="path468"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 281.01,504.93 0.33,4.41 1.02,3.84 1.65,3.06 2.22,2.19 2.67,1.23 3.06,0.18 3.27,-0.87" />
                                                        &#xa;
                                                        <path
                                                            id="path469"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 281.31,421.56 -0.3,83.37" />
                                                        &#xa;
                                                        <path
                                                            id="path470"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 297.63,389.82 -3.18,2.25 -3.03,3.03 -2.82,3.69 -2.49,4.2 -2.01,4.56 -1.53,4.74 -0.93,4.71 -0.33,4.56" />
                                                        &#xa;
                                                        <path
                                                            id="path471"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 344.82,362.7 -47.19,27.12"
                                                            transform="matrix(1,0,0,-1,0,842)" />
                                                        &#xa;
                                                        <path
                                                            id="path476"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 398.79,476.58 3.3,-1.47 3.33,-1.77" />
                                                        &#xa;
                                                        <path
                                                            id="path566"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 434.36412,530.1543 -47.19,-27.12" />
                                                        &#xa;
                                                        <path
                                                            id="path567"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 388.97423,504.373 -47.19,-27.12" />
                                                        &#xa;
                                                        <path
                                                            id="path477"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 295.23,518.97 89.82,35.64" />
                                                        &#xa;
                                                        <path
                                                            id="path478"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 377.67,554.94 287.85,519.3" />
                                                        &#xa;
                                                        <path
                                                            id="path491"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 483.78,513.69 4.17,-1.71" />
                                                        &#xa;
                                                        <path
                                                            id="path492"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 451.62,531.24 -0.39,-0.42 0.24,-0.66 0.93,-0.93 1.53,-1.14 2.13,-1.35 2.7,-1.53 3.24,-1.71 3.69,-1.83 4.11,-1.92 4.44,-2.01 4.68,-2.04 4.86,-2.01" />
                                                        &#xa;
                                                        <path
                                                            id="path493"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 692.88,626.97 451.62,531.24" />
                                                        &#xa;
                                                        <path
                                                            id="path494"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 735.96,613.74 -4.95,2.01 -4.98,1.92 -4.89,1.8 -4.71,1.68 -4.5,1.53 -4.17,1.32 -3.78,1.11 -3.33,0.9 -2.82,0.63 -2.25,0.39 -1.68,0.09 -1.02,-0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path495"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 740.13,612.06 -4.17,1.68" />
                                                        &#xa;
                                                        <path
                                                            id="path496"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 745.68,607.11 0.33,1.02 0.75,0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path497"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 494.58,508.71 0.51,0.06 0.39,-0.21" />
                                                        &#xa;
                                                        <path
                                                            id="path498"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 487.95,511.98 3.3,-1.5 3.33,-1.77" />
                                                        &#xa;
                                                        <path
                                                            id="path499"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 746.76,608.79 -3.33,1.77 -3.3,1.5 -0.75,-0.69 -0.24,-1.05 3.27,-1.47 3.27,-1.74" />
                                                        &#xa;
                                                        <path
                                                            id="path500"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 487.95,511.98 h 0.63" />
                                                        &#xa;
                                                        <path
                                                            id="path501"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 483.78,513.69 h 0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path502"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 451.62,531.24 0.09,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path503"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 457.89,526.08 -2.25,1.35 -1.8,1.17 -1.29,0.96 -0.81,0.78 -0.27,0.54 0.24,0.3" />
                                                        &#xa;
                                                        <path
                                                            id="path504"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 692.88,626.97 0.09,-0.03 -241.26,-95.76" />
                                                        &#xa;
                                                        <path
                                                            id="path505"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 692.97,626.94 0.9,0.06 1.53,-0.18 2.13,-0.51 2.67,-0.75 3.21,-1.02 3.69,-1.26 4.08,-1.5 4.41,-1.68 4.65,-1.83 4.86,-2.01 4.92,-2.07 4.95,-2.16 0.24,1.02 0.75,0.69" />
                                                        &#xa;
                                                        <path
                                                            id="path506"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 734.97,612.03 4.17,-1.71" />
                                                        &#xa;
                                                        <path
                                                            id="path507"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 495.3,508.71 -3.36,1.77 -3.36,1.5" />
                                                        &#xa;
                                                        <path
                                                            id="path508"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 488.58,511.98 -4.14,1.71" />
                                                        &#xa;
                                                        <path
                                                            id="path509"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 457.89,526.08 2.34,-1.29 2.7,-1.41 3,-1.5 3.3,-1.56 7.29,-3.3 7.92,-3.33" />
                                                        &#xa;
                                                        <path
                                                            id="path524"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 745.68,607.11 v -1.23" />
                                                        &#xa;
                                                        <path
                                                            id="path525"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="M 741.33,599.16 502.11,504.21" />
                                                        &#xa;
                                                        <path
                                                            id="path526"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 741.33,599.16 1.68,1.02 1.41,1.65 0.93,2.01 0.33,2.04" />
                                                        &#xa;
                                                        <path
                                                            id="path528"
                                                            transform="matrix(1,0,0,-1,0,842)"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 692.97,626.94 48.36,-27.78" />
                                                        &#xa;
                                                        <path
                                                            id="path569"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 530.67708,485.3093 -80.85,32.1" />
                                                        &#xa;
                                                    </g>
                                                    &#xa;
                                                    <g
                                                        id="g801"
                                                        transform="matrix(0.43208575,-0.90183252,-0.90183252,-0.43208575,44.547294,736.68214)">
                                                        &#xa;
                                                        <path
                                                            id="path570"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 568.16423,92.701328 -3.84,0.36 -3.63,-0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path571"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 557.99423,88.801328 2.76,-0.33" />
                                                        &#xa;
                                                        <path
                                                            id="path572"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.17423,39.631328 2.19,2.88 1.62,3.51" />
                                                        &#xa;
                                                        <path
                                                            id="path573"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 587.57423,41.761328 -1.11,-2.55" />
                                                        &#xa;
                                                        <path
                                                            id="path574"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 596.75423,66.181328 -0.33,-0.54" />
                                                        &#xa;
                                                        <path
                                                            id="path575"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 585.83423,78.031328 0.48,0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path576"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 586.31423,78.181328 1.08,-3.3 1.74,-3.06 2.28,-2.64 2.61,-1.92 2.73,-1.08" />
                                                        &#xa;
                                                        <path
                                                            id="path577"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 593.03423,88.651328 -2.49,-0.24 -2.1,-1.14 -1.53,-2.01 -0.78,-2.67 -0.03,-3.12" />
                                                        &#xa;
                                                        <path
                                                            id="path578"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 585.59423,79.351328 0.51,0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path579"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 604.52423,76.471328 -1.05,3.3 -1.74,3.06 -2.28,2.64 -2.61,1.92 -2.73,1.08" />
                                                        &#xa;
                                                        <path
                                                            id="path580"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 597.80423,66.001328 -0.33,-0.57" />
                                                        &#xa;
                                                        <path
                                                            id="path581"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 597.80423,66.001328 2.52,0.24 2.1,1.14 1.5,2.01 0.81,2.67 0.03,3.12" />
                                                        &#xa;
                                                        <path
                                                            id="path582"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 594.11423,88.471328 -1.98,0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path583"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 604.40423,70.561328 -0.6,-1.92" />
                                                        &#xa;
                                                        <path
                                                            id="path584"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 594.20423,98.881328 0.06,-0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path585"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 594.05423,98.971328 0.03,-0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path586"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 575.66423,95.761328 -0.12,-0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path587"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 575.54423,95.611328 -8.64,-4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path588"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 566.96423,90.781328 v -0.03 l -0.06,-0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path589"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 565.58423,67.771328 0.06,-0.12 0.03,-0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path590"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 565.58423,67.771328 8.67,4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path591"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 574.25423,72.751328 0.09,-0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path592"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 574.34423,72.481328 -8.67,-4.95" />
                                                        &#xa;
                                                        <path
                                                            id="path593"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.41423,52.831328 0.24,-0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path594"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.65423,52.711328 -8.67,-4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path595"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 582.74423,47.851328 0.15,-0.06 0.09,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path596"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 582.74423,47.851328 8.67,4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path597"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 610.13423,56.071328 -0.12,-0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path598"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 601.34423,50.941328 h 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path599"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 601.34423,50.941328 8.67,4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path600"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 611.45423,78.931328 v -0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path601"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 611.30423,79.291328 0.15,-0.45" />
                                                        &#xa;
                                                        <path
                                                            id="path602"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 611.30423,79.291328 0.03,-0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path603"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 574.28423,72.871328 -0.03,-0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path604"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 574.28423,72.871328 0.18,-0.45" />
                                                        &#xa;
                                                        <path
                                                            id="path605"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 574.34423,72.481328 0.12,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path606"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 588.59423,95.701328 3.36,0.03 3.54,-0.93 3.54,-1.89 3.33,-2.7 2.97,-3.42 2.43,-3.93 1.77,-4.23 0.99,-4.29 0.21,-4.14 -0.66,-3.75 -1.41,-3.18 -2.16,-2.4 -2.73,-1.53 -3.21,-0.57 -3.45,0.45 -3.57,1.44 -3.48,2.31 -3.15,3.09 -2.73,3.69 -2.1,4.11 -1.41,4.29 -0.6,4.26 0.24,3.96 1.02,3.48 1.8,2.82 2.46,1.98 3,1.05" />
                                                        &#xa;
                                                        <path
                                                            id="path607"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 593.99423,98.971328 -1.89,-0.12 -1.92,-0.15 -4.02,-0.57 -4.62,-0.93 -2.67,-0.63 -3.09,-0.78" />
                                                        &#xa;
                                                        <path
                                                            id="path608"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 593.99423,98.971328 0.39,-0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path609"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 594.38423,98.791328 2.88,-2.34 2.55,-2.25 4.29,-4.44 3.72,-4.77 1.74,-2.7 1.74,-3" />
                                                        &#xa;
                                                        <path
                                                            id="path610"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 611.45423,78.841328 0.42,-2.76 0.24,-2.64 -0.03,-5.19 -0.6,-5.55 -0.54,-3.09 -0.78,-3.42" />
                                                        &#xa;
                                                        <path
                                                            id="path611"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 610.16423,56.191328 -0.21,-0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path612"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 609.95423,55.921328 -1.89,-0.12 -1.92,-0.15 -4.02,-0.6 -4.62,-0.9 -2.67,-0.63 -3.09,-0.78" />
                                                        &#xa;
                                                        <path
                                                            id="path613"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.38423,52.921328 0.36,-0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path614"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.38423,52.921328 -1.74,3 -1.74,2.7 -3.72,4.8 -4.29,4.44 -2.55,2.22 -2.88,2.34" />
                                                        &#xa;
                                                        <path
                                                            id="path615"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 574.28423,72.871328 0.75,3.42 0.57,3.12 0.6,5.52 v 5.19 l -0.21,2.64 -0.42,2.76" />
                                                        &#xa;
                                                        <path
                                                            id="path616"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 575.78423,95.791328 -0.21,-0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path617"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 604.49423,76.411328 0.24,-1.23" />
                                                        &#xa;
                                                        <path
                                                            id="path618"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 604.82423,74.161328 -0.09,-2.58 -0.6,-2.28 -1.11,-1.86 -1.53,-1.35" />
                                                        &#xa;
                                                        <path
                                                            id="path619"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 588.77423,88.231328 1.95,0.66 h 2.16 l 2.28,-0.63 2.25,-1.2" />
                                                        &#xa;
                                                        <path
                                                            id="path620"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 593.57423,88.741328 2.34,-0.87" />
                                                        &#xa;
                                                        <path
                                                            id="path621"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 604.46423,76.291328 0.18,-1.11" />
                                                        &#xa;
                                                        <path
                                                            id="path622"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 604.79423,72.421328 -0.45,-2.46" />
                                                        &#xa;
                                                        <path
                                                            id="path623"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 583.64423,39.541328 0.84,0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path624"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 556.85423,86.191328 0.78,0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path625"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 572.21423,94.321328 0.93,0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path626"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 561.20423,79.741328 0.9,3.84 1.92,3.69 2.88,3.51 0.93,1.53 1.8,1.2 2.58,0.81" />
                                                        &#xa;
                                                        <path
                                                            id="path627"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 561.20423,79.741328 -0.06,-1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path628"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 569.96423,54.811328 -2.34,3.75 -1.47,4.32 -0.57,4.77 -2.49,3.45 -1.5,3.69 -0.45,3.81" />
                                                        &#xa;
                                                        <path
                                                            id="path629"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 569.96423,54.811328 0.84,-0.96" />
                                                        &#xa;
                                                        <path
                                                            id="path630"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 590.63423,44.611328 -2.91,0.09 -2.64,1.05 -2.22,1.98 -4.62,1.2 -4.05,2.07 -3.39,2.85" />
                                                        &#xa;
                                                        <path
                                                            id="path631"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 590.63423,44.611328 0.93,0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path632"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 601.46423,50.941328 -3.36,-2.94 -3.33,-2.07 -3.21,-1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path633"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 601.46423,51.001328 v -0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path634"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 573.14423,94.471328 0.33,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path635"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 581.78423,74.971328 -1.2,4.26 -0.39,4.17 0.42,3.84 1.23,3.3 1.98,2.61 2.58,1.74 3.06,0.78 3.39,-0.18 3.54,-1.17 3.48,-2.1 3.24,-2.88 2.85,-3.54 2.25,-3.99 1.56,-4.26 0.81,-4.23 -0.03,-4.05 -0.84,-3.6 -1.59,-2.97 -2.31,-2.16 -2.85,-1.29 -3.24,-0.3 -3.48,0.69 -3.54,1.65 -3.39,2.49 -3.06,3.24 -2.55,3.78 -1.92,4.17" />
                                                        &#xa;
                                                        <path
                                                            id="path636"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 586.43423,75.751328 -0.9,3.48 -0.09,3.3 0.72,2.88 1.47,2.22 2.1,1.38 2.55,0.45 2.82,-0.54 2.85,-1.47 2.64,-2.31 2.22,-2.91 1.62,-3.33 0.9,-3.48 0.09,-3.3 -0.72,-2.88 -1.47,-2.22 -2.1,-1.38 -2.58,-0.45 -2.82,0.54 -2.82,1.47 -2.64,2.31 -2.22,2.91 -1.62,3.33" />
                                                        &#xa;
                                                        <path
                                                            id="path637"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 588.89423,88.291328 2.37,0.75 2.7,-0.18 2.79,-1.14 2.7,-1.98 2.31,-2.67 1.83,-3.15 1.11,-3.36 0.39,-3.33 -0.45,-2.97 -1.17,-2.43 -1.86,-1.68" />
                                                        &#xa;
                                                        <path
                                                            id="path638"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 572.21423,94.321328 0.93,0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path639"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 566.96423,90.751328 -0.06,0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path640"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 561.14423,78.601328 0.06,1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path641"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 566.90423,90.631328 -1.32,-22.86" />
                                                        &#xa;
                                                        <path
                                                            id="path642"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 565.64423,67.651328 h -0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path643"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 601.46423,51.001328 v -0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path644"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.56423,44.791328 -0.93,-0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path645"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 582.89423,47.791328 -0.03,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path646"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 582.98423,47.731328 18.36,3.21" />
                                                        &#xa;
                                                        <path
                                                            id="path647"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 570.80423,53.851328 -0.84,0.96" />
                                                        &#xa;
                                                        <path
                                                            id="path648"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 565.67423,67.531328 17.07,-19.68" />
                                                        &#xa;
                                                        <path
                                                            id="path649"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 610.16423,56.191328 -0.03,-0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path650"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.65423,52.711328 0.09,0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path651"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 609.95423,55.921328 h 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path652"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 591.38423,52.921328 0.03,-0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path653"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 575.54423,95.611328 0.03,-0.09" />
                                                        &#xa;
                                                        <path
                                                            id="path654"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 593.99423,98.971328 h 0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path655"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 575.66423,95.761328 0.12,0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path656"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 594.26423,98.851328 0.12,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path657"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 575.60423,95.731328 -8.64,-4.95" />
                                                        &#xa;
                                                        <path
                                                            id="path658"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 610.04423,55.921328 -8.64,-4.98" />
                                                        &#xa;
                                                        <path
                                                            id="path659"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 611.33423,79.201328 0.12,-0.27" />
                                                        &#xa;
                                                        <path
                                                            id="path660"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 588.77423,88.231328 2.25,0.69 2.55,-0.18" />
                                                        &#xa;
                                                        <path
                                                            id="path661"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 604.34423,69.961328 -1.14,-2.28 -1.71,-1.59" />
                                                        &#xa;
                                                        <path
                                                            id="path662"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 583.67423,39.541328 0.81,0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path663"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 556.85423,86.191328 0.78,0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path664"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 584.48423,39.961328 11.31,6.51" />
                                                        &#xa;
                                                        <path
                                                            id="path665"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 557.63423,86.671328 11.34,6.51" />
                                                        &#xa;
                                                        <path
                                                            id="path666"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 601.61423,66.151328 -1.56,-0.6 -1.74,-0.18 -1.86,0.27 -1.92,0.72 -1.89,1.14 -1.8,1.53 -1.62,1.83 -1.41,2.1 -1.08,2.25 -0.78,2.34 -0.42,2.31 -0.03,2.22 0.36,2.01 0.69,1.77 1.02,1.41 1.32,1.02" />
                                                        &#xa;
                                                        <path
                                                            id="path667"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 594.08423,98.941328 0.12,-0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path668"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 326.45423,57.301328 5.88,3.87 5.82,4.71 5.67,5.49 5.46,6.21 5.19,6.84 4.86,7.38 4.47,7.89 4.05,8.250002 3.54,8.55 3,8.7 2.43,8.82 1.83,8.76" />
                                                        &#xa;
                                                        <path
                                                            id="path669"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 378.80423,181.05133 -0.96,3.99 -1.2,3.81" />
                                                        &#xa;
                                                        <path
                                                            id="path670"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 378.65423,142.77133 0.15,38.28" />
                                                        &#xa;
                                                        <path
                                                            id="path671"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 415.61423,21.931328 h 0.72" />
                                                        &#xa;
                                                        <path
                                                            id="path672"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.36423,-68.518672 -239.28,94.98" />
                                                        &#xa;
                                                        <path
                                                            id="path673"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 666.71423,-75.238672 -0.33,2.04 -0.93,2.01 -1.41,1.62 -1.68,1.05" />
                                                        &#xa;
                                                        <path
                                                            id="path674"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 666.71423,-76.468672 v 1.23" />
                                                        &#xa;
                                                        <path
                                                            id="path675"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 667.79423,-78.148672 -0.75,0.66 -0.33,1.02" />
                                                        &#xa;
                                                        <path
                                                            id="path676"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 809.15423,-28.048672 -1.83,-8.79 -2.43,-8.79 -3.03,-8.73 -3.51,-8.52 -4.05,-8.28 -4.47,-7.86 -4.86,-7.41 -5.19,-6.84 -5.46,-6.21 -5.67,-5.459998 -5.82,-4.71 -5.88,-3.87" />
                                                        &#xa;
                                                        <path
                                                            id="path677"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 809.30423,10.231328 -0.15,-38.28" />
                                                        &#xa;
                                                        <path
                                                            id="path678"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 788.24423,40.051328 4.26,-2.16 3.87,-2.88 3.51,-3.66 3.06,-4.35 2.61,-5.01 2.13,-5.61 1.62,-6.15" />
                                                        &#xa;
                                                        <path
                                                            id="path679"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 809.30423,10.231328 -80.85,32.07" />
                                                        &#xa;
                                                        <path
                                                            id="path680"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 704.87423,67.441328 -84,33.330002" />
                                                        &#xa;
                                                        <path
                                                            id="path681"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.87423,128.13133 -84,33.36" />
                                                        &#xa;
                                                        <path
                                                            id="path682"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 459.65423,148.95133 -80.85,32.1" />
                                                        &#xa;
                                                        <path
                                                            id="path683"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 728.30423,4.0213282 80.85,-32.0700002" />
                                                        &#xa;
                                                        <path
                                                            id="path684"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 378.65423,142.77133 80.88,-32.07" />
                                                        &#xa;
                                                        <path
                                                            id="path685"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 467.57423,76.651328 84,-33.36" />
                                                        &#xa;
                                                        <path
                                                            id="path686"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 620.54423,15.931328 84.03,-33.33" />
                                                        &#xa;
                                                        <path
                                                            id="path687"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 716.24423,57.841328 2.64,-3.87 2.7,-3.96 1.47,-2.1 1.59,-2.16 1.77,-1.98 0.99,-0.87 1.05,-0.6" />
                                                        &#xa;
                                                        <path
                                                            id="path688"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 459.65423,148.95133 0.96,-0.18 0.78,0.15 1.08,0.87 0.75,1.23 0.48,1.32 0.42,2.73 -0.21,2.91" />
                                                        &#xa;
                                                        <path
                                                            id="path689"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 355.56029,218.97062 4.26,-2.16 3.87,-2.88 3.51,-3.66 3.06,-4.35 2.61,-5.01 2.13,-5.61 1.62,-6.15" />
                                                        &#xa;
                                                        <path
                                                            id="path690"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 728.45423,42.301328 -0.15,-38.2799998" />
                                                        &#xa;
                                                        <path
                                                            id="path691"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 463.67423,90.511328 0.24,5.52 -0.39,5.310002 -0.48,2.67 -0.72,2.67 -1.08,2.37 -0.78,0.99 -0.93,0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path692"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 728.30423,4.0213282 -1.02,0.15 -1.02,-0.3 -1.77,-1.23 -1.62,-1.74 -1.5,-1.89 -2.7,-4.05 -2.67,-4.56" />
                                                        &#xa;
                                                        <path
                                                            id="path693"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 459.53423,110.70133 0.12,38.25" />
                                                        &#xa;
                                                        <path
                                                            id="path694"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 464.12423,155.58133 -0.21,-60.510002" />
                                                        &#xa;
                                                        <path
                                                            id="path695"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 704.87423,67.441328 1.65,-0.78 1.77,-1.05 1.65,-1.14 1.53,-1.26 2.73,-2.73 2.04,-2.64" />
                                                        &#xa;
                                                        <path
                                                            id="path696"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 463.91423,157.98133 -0.18,1.89 0.36,1.5 0.48,0.45 0.75,0.21 1.11,-0.09 1.44,-0.45" />
                                                        &#xa;
                                                        <path
                                                            id="path697"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 467.57423,76.651328 -1.44,0.9 -1.11,1.41 -0.75,1.65 -0.48,1.89 -0.33,4.08 0.21,3.93" />
                                                        &#xa;
                                                        <path
                                                            id="path698"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 716.00423,-9.5986718 -2.07,-3.2100002 -2.73,-2.88 -1.56,-1.05 -1.65,-0.72 -1.77,-0.27 -1.65,0.33" />
                                                        &#xa;
                                                        <path
                                                            id="path699"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 716.24423,57.841328 -0.24,-67.4399998" />
                                                        &#xa;
                                                        <path
                                                            id="path700"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 704.57423,-17.398672 0.3,84.84" />
                                                        &#xa;
                                                        <path
                                                            id="path701"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 467.87423,161.49133 -0.3,-84.840002" />
                                                        &#xa;
                                                        <path
                                                            id="path702"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.76423,109.65133 1.77,-0.84 1.86,-1.05 1.56,-1.11 1.35,-1.14 1.41,-1.23 1.56,-1.26 1.77,-1.29 0.93,-0.54 0.9,-0.42" />
                                                        &#xa;
                                                        <path
                                                            id="path703"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.87423,128.13133 0.78,-0.21 0.57,-0.06 0.63,0.33 0.09,0.6 -0.33,0.81 -0.33,0.72 0.06,0.45 0.66,0.09 1.32,-0.39" />
                                                        &#xa;
                                                        <path
                                                            id="path704"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 554.93423,28.831328 -1.32,1.11 -0.63,1.74 -0.06,1.98 0.33,2.1 0.36,2.22 -0.09,2.13 -0.6,1.95 -0.6,0.75 -0.75,0.48" />
                                                        &#xa;
                                                        <path
                                                            id="path705"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 620.54423,15.931328 -0.87,0.15 -0.93,-0.15 -1.8,-0.99 -1.56,-1.47 -1.41,-1.8 -1.38,-1.7099998 -1.56,-1.32 -1.86,-0.75 -1.8,0.12" />
                                                        &#xa;
                                                        <path
                                                            id="path706"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 554.99423,40.081328 -0.06,-11.25" />
                                                        &#xa;
                                                        <path
                                                            id="path707"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 555.26423,119.19133 -0.39,-3.42 -1.11,-2.91 -1.8,-2.25 -3.48,-3.78 -2.76,-4.59 -2.04,-5.250002 -1.23,-5.85 -0.45,-6.3 0.39,-6.63 1.2,-6.81 1.98,-6.84 2.73,-6.75 3.45,-6.54 1.77,-3.66 1.08,-3.81 0.39,-3.72" />
                                                        &#xa;
                                                        <path
                                                            id="path708"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 555.32423,130.47133 -0.06,-11.28" />
                                                        &#xa;
                                                        <path
                                                            id="path709"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.70423,98.371328 0.06,11.280002" />
                                                        &#xa;
                                                        <path
                                                            id="path710"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.43423,19.291328 0.39,3.39 1.11,2.94 1.8,2.25 3.48,3.78 2.76,4.59 2.04,5.25 1.23,5.85 0.45,6.3 -0.39,6.6 -1.2,6.81 -1.98,6.87 -2.76,6.75 -3.42,6.51 -1.77,3.69 -1.08,3.78 -0.39,3.72" />
                                                        &#xa;
                                                        <path
                                                            id="path711"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.37423,8.0113282 0.06,11.2799998" />
                                                        &#xa;
                                                        <path
                                                            id="path712"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.87423,125.28133 v 2.85" />
                                                        &#xa;
                                                        <path
                                                            id="path713"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.60423,46.171328 -0.33,2.07 -0.87,2.07 -2.7,4.86 -2.37,5.04 -2.04,5.13 -1.68,5.16 -1.29,5.19 -0.96,5.16 -0.57,5.1 -0.18,4.98 0.21,4.8 0.6,4.620002 0.99,4.41 1.35,4.14 1.71,3.81 2.07,3.48 2.4,3.15 2.7,2.76 0.9,1.35 0.33,1.83" />
                                                        &#xa;
                                                        <path
                                                            id="path714"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.57423,43.291328 0.03,2.88" />
                                                        &#xa;
                                                        <path
                                                            id="path715"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 620.87423,100.77133 -0.03,-2.880002" />
                                                        &#xa;
                                                        <path
                                                            id="path716"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 620.84423,97.891328 -2.04,0.54 -2.34,0.09 -2.19,-0.39" />
                                                        &#xa;
                                                        <path
                                                            id="path717"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 614.27423,98.131328 0.03,7.380002" />
                                                        &#xa;
                                                        <path
                                                            id="path718"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 620.84423,97.891328 0.33,-2.07 0.87,-2.04 -1.62,-0.99 -1.95,-1.17 -1.98,-1.14 -0.93,1.86 -0.72,1.95 -0.42,1.95 -0.15,1.89" />
                                                        &#xa;
                                                        <path
                                                            id="path719"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 622.04423,93.781328 2.67,-4.89 2.4,-5.04 2.01,-5.13 1.68,-5.16 1.32,-5.19 0.96,-5.16 0.57,-5.1 0.18,-4.98 -0.21,-4.8 -0.6,-4.62 -0.99,-4.41 -1.35,-4.11 -1.71,-3.84 -2.07,-3.48 -2.4,-3.15 -2.7,-2.76 -1.62,1.68 -1.95,1.05 -1.98,0.24 2.49,2.52 2.19,2.85 1.89,3.18 1.56,3.51 1.23,3.75 0.9,4.05 0.54,4.2 0.21,4.38 -0.18,4.56 -0.51,4.65 -0.87,4.71 -1.2,4.74 -1.53,4.71 -1.86,4.68 -2.16,4.62 -2.46,4.44" />
                                                        &#xa;
                                                        <path
                                                            id="path720"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 621.80423,21.961328 -0.9,-1.32 -0.33,-1.83 -2.07,0.51 -2.31,0.09 -2.19,-0.36 0.15,1.77 0.45,1.62 0.69,1.38 0.96,1.11" />
                                                        &#xa;
                                                        <path
                                                            id="path721"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 613.97423,11.671328 0.03,7.38" />
                                                        &#xa;
                                                        <path
                                                            id="path722"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 620.57423,18.811328 -0.03,-2.88" />
                                                        &#xa;
                                                        <path
                                                            id="path723"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.60423,46.171328 1.5,-0.93 0.54,-1.17" />
                                                        &#xa;
                                                        <path
                                                            id="path724"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 550.40423,50.311328 0.93,0.57 0.33,0.24" />
                                                        &#xa;
                                                        <path
                                                            id="path725"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 550.64423,122.10133 1.02,-2.01 0.24,-2.04 -0.6,-1.71 -2.49,-2.52 -2.19,-2.88" />
                                                        &#xa;
                                                        <path
                                                            id="path726"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.87423,125.28133 1.53,-0.93 0.54,-1.17" />
                                                        &#xa;
                                                        <path
                                                            id="path727"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 552.26423,117.48133 -0.96,-1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path728"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 555.26423,119.19133 -1.02,0.51 -0.69,0.63" />
                                                        &#xa;
                                                        <path
                                                            id="path729"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.96423,110.61133 -1.02,2.01 -0.24,2.04 0.6,1.68" />
                                                        &#xa;
                                                        <path
                                                            id="path730"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 551.60423,51.211328 0.15,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path731"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 553.64423,40.861328 1.35,-0.78" />
                                                        &#xa;
                                                        <path
                                                            id="path732"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.43423,19.291328 2.04,-0.54 2.34,-0.09 2.19,0.39" />
                                                        &#xa;
                                                        <path
                                                            id="path733"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 610.73423,27.871328 1.62,-1.68 1.95,-1.05 1.95,-0.21" />
                                                        &#xa;
                                                        <path
                                                            id="path734"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 610.94423,87.181328 1.65,0.99 1.95,1.17 1.95,1.14" />
                                                        &#xa;
                                                        <path
                                                            id="path735"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.70423,98.371328 2.07,-0.51 2.31,-0.09 2.19,0.36" />
                                                        &#xa;
                                                        <path
                                                            id="path736"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 553.64423,44.071328 -0.03,-5.4" />
                                                        &#xa;
                                                        <path
                                                            id="path737"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 546.62423,110.94133 -1.53,-2.55 -1.32,-2.79 -1.11,-3.03 -0.87,-3.300002 -0.63,-3.51 -0.36,-3.66 -0.12,-3.84 0.15,-3.99 0.45,-4.08 0.69,-4.17 0.99,-4.2 1.23,-4.23 1.5,-4.2 1.77,-4.2 1.98,-4.08 2.22,-3.99 1.44,-3.36 0.42,-1.8 0.12,-1.89" />
                                                        &#xa;
                                                        <path
                                                            id="path738"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 553.94423,123.18133 -0.39,-2.88 -1.29,-2.82" />
                                                        &#xa;
                                                        <path
                                                            id="path739"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 553.94423,128.58133 v -5.4" />
                                                        &#xa;
                                                        <path
                                                            id="path740"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.76423,109.65133 -52.44,20.82" />
                                                        &#xa;
                                                        <path
                                                            id="path741"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 554.93423,28.831328 52.44,-20.8199998" />
                                                        &#xa;
                                                        <path
                                                            id="path742"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 685.82423,-54.928672 0.93,-0.72 0.42,-1.08 -0.18,-2.37 -0.96,-2.37 -1.35,-2.25 -3.39,-4.08 -3.9,-3.6 -4.77,-3.66 -4.83,-3.09" />
                                                        &#xa;
                                                        <path
                                                            id="path743"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 444.56423,40.801328 241.26,-95.73" />
                                                        &#xa;
                                                        <path
                                                            id="path744"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 415.61423,21.931328 4.83,3.09 4.77,3.66 4.08,3.51 4.41,3.69 2.4,1.83 2.64,1.68 2.88,1.32 1.53,0.3 1.41,-0.21" />
                                                        &#xa;
                                                        <path
                                                            id="path745"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 666.71423,-76.468672 4.74,3.03 4.68,3.6 3.84,3.27 3.42,3.66 1.44,1.98 1.11,2.07 0.42,2.07 -0.24,0.9 -0.72,0.6" />
                                                        &#xa;
                                                        <path
                                                            id="path746"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 685.40423,-55.288672 -241.26,95.76" />
                                                        &#xa;
                                                        <path
                                                            id="path747"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 444.14423,40.471328 -1.17,0.12 -1.35,-0.3 -2.67,-1.26" />
                                                        &#xa;
                                                        <path
                                                            id="path748"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 425.21423,28.681328 0.72,0.03" />
                                                        &#xa;
                                                        <path
                                                            id="path749"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 676.13423,-69.838672 0.42,-0.9 0.84,-0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path750"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 685.40423,-55.288672 0.42,0.36" />
                                                        &#xa;
                                                        <path
                                                            id="path751"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 444.14423,40.471328 0.42,0.33" />
                                                        &#xa;
                                                        <path
                                                            id="path752"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 438.95423,39.031328 -3.6,-2.43 -3.3,-2.67 -3.09,-2.67 -3.03,-2.55 -4.77,-3.66 -4.83,-3.12" />
                                                        &#xa;
                                                        <path
                                                            id="path753"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 577.70423,96.301328 -4.23,0.84 -4.02,-0.09 -3.72,-0.96 -3.27,-1.89 -2.73,-2.7 -2.1,-3.45 -1.41,-4.08 -0.66,-4.56 0.09,-4.92 0.87,-5.13" />
                                                        &#xa;
                                                        <path
                                                            id="path754"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 568.94423,47.731328 3.93,-3.27 4.11,-2.55 4.23,-1.74 4.14,-0.87 h 3.99 l 3.66,0.9 3.27,1.74 2.76,2.55 2.16,3.3 1.5,3.9" />
                                                        &#xa;
                                                        <path
                                                            id="path755"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 607.22423,54.301328 -1.14,-4.74 -1.98,-4.11 -2.67,-3.36 -3.36,-2.46 -3.87,-1.53 -4.29,-0.51 -4.56,0.48 -4.68,1.5 -4.68,2.46 -4.5,3.33 -4.17,4.08 -3.75,4.74 -3.15,5.22 -2.49,5.52 -1.74,5.67 -0.9,5.61 -0.09,5.43 0.75,4.98 1.56,4.44 2.34,3.75 3.03,2.94 3.6,1.98 4.11,1.050002 h 4.44 l 4.65,-0.990002 4.71,-1.98" />
                                                        &#xa;
                                                        <path
                                                            id="path756"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 599.75423,49.321328 -1.5,-3.51 -2.04,-3 -2.55,-2.34" />
                                                        &#xa;
                                                        <path
                                                            id="path757"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 562.70423,94.381328 3.57,1.05 3.87,0.21 4.08,-0.69" />
                                                        &#xa;
                                                        <path
                                                            id="path758"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.36423,-68.518672 23.04,13.23" />
                                                        &#xa;
                                                        <path
                                                            id="path759"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 788.24423,40.051328 -411.54,163.320002" />
                                                        &#xa;
                                                        <path
                                                            id="path760"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 358.94423,-2.3986718 340.68,-135.1799982" />
                                                        &#xa;
                                                        <path
                                                            id="path761"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 692.24423,-137.93867 -337.35,133.8899982" />
                                                        &#xa;
                                                        <path
                                                            id="path762"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 699.62423,-137.57867 -2.61,-0.78 -2.49,-0.12 -2.28,0.54" />
                                                        &#xa;
                                                        <path
                                                            id="path763"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 749.96423,-116.99867 -50.34,-20.58" />
                                                        &#xa;
                                                        <path
                                                            id="path764"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 756.59423,-113.72867 -3.33,-1.8 -3.3,-1.47" />
                                                        &#xa;
                                                        <path
                                                            id="path765"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 486.11423,-56.128672 -4.83,1.68 -2.64,1.02 -2.85,1.11 -3.03,1.2 -3.15,1.29 -6.51,2.85" />
                                                        &#xa;
                                                        <path
                                                            id="path766"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 305.72423,-24.178672 53.22,21.7800002" />
                                                        &#xa;
                                                        <path
                                                            id="path767"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 298.34423,-24.508672 2.28,-0.54 2.49,0.12 2.61,0.75" />
                                                        &#xa;
                                                        <path
                                                            id="path768"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 215.90423,11.461328 103.56,42.39" />
                                                        &#xa;
                                                        <path
                                                            id="path769"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 201.68423,25.501328 0.33,-4.41 1.02,-3.84 1.65,-3.06 2.22,-2.19 2.67,-1.23 3.06,-0.18 3.27,0.87" />
                                                        &#xa;
                                                        <path
                                                            id="path770"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 201.98423,108.87133 -0.3,-83.370002" />
                                                        &#xa;
                                                        <path
                                                            id="path771"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 218.30423,140.61133 -3.18,-2.25 -3.03,-3.03 -2.82,-3.69 -2.49,-4.2 -2.01,-4.56 -1.53,-4.74 -0.93,-4.71 -0.33,-4.56" />
                                                        &#xa;
                                                        <path
                                                            id="path772"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 265.49423,167.73133 -47.19,-27.12" />
                                                        &#xa;
                                                        <path
                                                            id="path773"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 319.46423,53.851328 3.3,1.47 3.33,1.77" />
                                                        &#xa;
                                                        <path
                                                            id="path774"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 355.03835,218.58563 -47.19,-27.12" />
                                                        &#xa;
                                                        <path
                                                            id="path775"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 309.64846,192.80433 -47.19,-27.12" />
                                                        &#xa;
                                                        <path
                                                            id="path776"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 215.90423,11.461328 89.82,-35.64" />
                                                        &#xa;
                                                        <path
                                                            id="path777"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 298.34423,-24.508672 -89.82,35.64" />
                                                        &#xa;
                                                        <path
                                                            id="path778"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 404.45423,16.741328 4.17,1.71" />
                                                        &#xa;
                                                        <path
                                                            id="path779"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 372.29423,-0.8086718 -0.39,0.42 0.24,0.66 0.93,0.93 1.53,1.14 2.13,1.35 2.7,1.53 3.24,1.71 3.69,1.83 4.11,1.9199998 4.44,2.01 4.68,2.04 4.86,2.01" />
                                                        &#xa;
                                                        <path
                                                            id="path780"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 613.55423,-96.538672 -241.26,95.7300002" />
                                                        &#xa;
                                                        <path
                                                            id="path781"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 656.63423,-83.308672 -4.95,-2.01 -4.98,-1.92 -4.89,-1.8 -4.71,-1.68 -4.5,-1.53 -4.17,-1.32 -3.78,-1.11 -3.33,-0.9 -2.82,-0.63 -2.25,-0.39 -1.68,-0.09 -1.02,0.15" />
                                                        &#xa;
                                                        <path
                                                            id="path782"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 660.80423,-81.628672 -4.17,-1.68" />
                                                        &#xa;
                                                        <path
                                                            id="path783"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 666.35423,-76.678672 0.33,-1.02 0.75,-0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path784"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 415.25423,21.721328 0.51,-0.06 0.39,0.21" />
                                                        &#xa;
                                                        <path
                                                            id="path785"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 408.62423,18.451328 3.3,1.5 3.33,1.77" />
                                                        &#xa;
                                                        <path
                                                            id="path786"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 667.43423,-78.358672 -3.33,-1.77 -3.3,-1.5 -0.75,0.69 -0.24,1.05 3.27,1.47 3.27,1.74" />
                                                        &#xa;
                                                        <path
                                                            id="path787"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 408.62423,18.451328 h 0.63" />
                                                        &#xa;
                                                        <path
                                                            id="path788"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 404.45423,16.741328 h 0.66" />
                                                        &#xa;
                                                        <path
                                                            id="path789"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 372.29423,-0.8086718 0.09,0.06" />
                                                        &#xa;
                                                        <path
                                                            id="path790"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 378.56423,4.3513282 -2.25,-1.35 -1.8,-1.17 -1.29,-0.96 -0.81,-0.78 -0.27,-0.54 0.24,-0.3" />
                                                        &#xa;
                                                        <path
                                                            id="path791"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 613.55423,-96.538672 0.09,0.03 -241.26,95.7600002" />
                                                        &#xa;
                                                        <path
                                                            id="path792"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 613.64423,-96.508672 0.9,-0.06 1.53,0.18 2.13,0.51 2.67,0.75 3.21,1.02 3.69,1.26 4.08,1.5 4.41,1.68 4.65,1.83 4.86,2.01 4.92,2.07 4.95,2.16 0.24,-1.02 0.75,-0.69" />
                                                        &#xa;
                                                        <path
                                                            id="path793"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 655.64423,-81.598672 4.17,1.71" />
                                                        &#xa;
                                                        <path
                                                            id="path794"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 415.97423,21.721328 -3.36,-1.77 -3.36,-1.5" />
                                                        &#xa;
                                                        <path
                                                            id="path795"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 409.25423,18.451328 -4.14,-1.71" />
                                                        &#xa;
                                                        <path
                                                            id="path796"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 378.56423,4.3513282 2.34,1.29 2.7,1.41 3,1.5 3.3,1.5599998 7.29,3.3 7.92,3.33" />
                                                        &#xa;
                                                        <path
                                                            id="path797"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 666.35423,-76.678672 v 1.23" />
                                                        &#xa;
                                                        <path
                                                            id="path798"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.00423,-68.728672 -239.22,94.95" />
                                                        &#xa;
                                                        <path
                                                            id="path799"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 662.00423,-68.728672 1.68,-1.02 1.41,-1.65 0.93,-2.01 0.33,-2.04" />
                                                        &#xa;
                                                        <path
                                                            id="path800"
                                                            stroke-width="0.99"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 613.64423,-96.508672 48.36,27.78" />
                                                        &#xa;
                                                        <path
                                                            id="path801"
                                                            stroke-width="1.41"
                                                            stroke-linecap="round"
                                                            stroke-linejoin="round"
                                                            fill="none"
                                                            :stroke="strokeColor"
                                                            d="m 451.35131,173.74063 -80.85,32.1" />
                                                        &#xa;
                                                    </g>
                                                    &#xa;
                                                </svg>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="3d8x6VWo7ciyXjxhZGTU-1">
                                        <g transform="translate(0.5,0.5)" />
                                        <g data-cell-id="3d8x6VWo7ciyXjxhZGTU-2">
                                            <g transform="translate(0.5,0.5)">
                                                <path
                                                    d="M 332 100.58 C 332 94.74 339 90 347.63 90 C 351.78 90 355.76 91.11 358.69 93.1 C 361.62 95.08 363.27 97.78 363.27 100.58 L 363.27 249.42 C 363.27 255.26 356.27 260 347.63 260 C 339 260 332 255.26 332 249.42 Z"
                                                    :fill="fillColor"
                                                    :stroke="strokeColor"
                                                    stroke-width="2"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 363.27 100.58 C 363.27 103.39 361.62 106.08 358.69 108.06 C 355.76 110.05 351.78 111.16 347.63 111.16 C 343.49 111.16 339.51 110.05 336.58 108.06 C 333.65 106.08 332 103.39 332 100.58"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-width="2"
                                                    stroke-miterlimit="10"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="3d8x6VWo7ciyXjxhZGTU-8">
                                        <g transform="translate(0.5,0.5)">
                                            <path
                                                d="M 345.01 98.82 L 290.34 67.26 L 199 120 L 78.49 189.58 L 148.5 230"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-width="2"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="6 6"
                                                pointer-events="stroke" />
                                            <ellipse
                                                cx="347.6"
                                                cy="100.32"
                                                rx="3"
                                                ry="3"
                                                :fill="fillColor"
                                                :stroke="strokeColor"
                                                stroke-width="2"
                                                pointer-events="all" />
                                        </g>
                                    </g>
                                    <g data-cell-id="3d8x6VWo7ciyXjxhZGTU-12">
                                        <g transform="translate(0.5,0.5)" />
                                        <g data-cell-id="3d8x6VWo7ciyXjxhZGTU-13">
                                            <g transform="translate(0.5,0.5)">
                                                <path
                                                    d="M 824 881.58 C 824 875.74 831 871 839.64 871 C 843.78 871 847.76 872.11 850.69 874.1 C 853.62 876.08 855.27 878.78 855.27 881.58 L 855.27 1030.42 C 855.27 1036.26 848.27 1041 839.64 1041 C 831 1041 824 1036.26 824 1030.42 Z"
                                                    :fill="fillColor"
                                                    :stroke="strokeColor"
                                                    stroke-width="2"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(120,839.64,956)"
                                                    pointer-events="all" />
                                                <path
                                                    d="M 855.27 881.58 C 855.27 884.39 853.62 887.08 850.69 889.06 C 847.76 891.05 843.78 892.16 839.64 892.16 C 835.49 892.16 831.51 891.05 828.58 889.06 C 825.65 887.08 824 884.39 824 881.58"
                                                    fill="none"
                                                    :stroke="strokeColor"
                                                    stroke-width="2"
                                                    stroke-miterlimit="10"
                                                    transform="rotate(120,839.64,956)"
                                                    pointer-events="all" />
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="3d8x6VWo7ciyXjxhZGTU-16">
                                        <g transform="translate(0.5,0.5)">
                                            <path
                                                d="M 908.6 995.5 L 1001.98 1049.41 L 949 1080 L 883.78 1117.66 L 763.77 1048.37"
                                                fill="none"
                                                :stroke="strokeColor"
                                                stroke-width="2"
                                                stroke-miterlimit="10"
                                                stroke-dasharray="6 6"
                                                pointer-events="stroke" />
                                            <ellipse
                                                cx="906"
                                                cy="994"
                                                rx="3"
                                                ry="3"
                                                :fill="fillColor"
                                                :stroke="strokeColor"
                                                stroke-width="2"
                                                pointer-events="all" />
                                        </g>
                                    </g>
                                    <g data-cell-id="y3XOAQ3aAnnzej_5DS3p-9" />
                                    <g data-cell-id="3d8x6VWo7ciyXjxhZGTU-6">
                                        <g transform="translate(0.5,0.5)">
                                            <rect
                                                x="33"
                                                y="230"
                                                width="231"
                                                height="148"
                                                rx="5.92"
                                                ry="5.92"
                                                :fill="fillColor"
                                                :stroke="strokeColor"
                                                stroke-width="2"
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
                                                                width: 229px;
                                                                height: 1px;
                                                                padding-top: 304px;
                                                                margin-left: 34px;
                                                            ">
                                                            <div>
                                                                <div v-if="rows[1]" class="text-h3">
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset.wcs === 1 &&
                                                                                hoveredOffset.axis === 0
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        X {{ rows[1].X }}
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
                                                                        Y {{ rows[1].Y }}
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
                                                                        Z {{ rows[1].Z }}
                                                                    </span>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </foreignObject>
                                                </switch>
                                            </g>
                                        </g>
                                    </g>
                                    <g data-cell-id="y3XOAQ3aAnnzej_5DS3p-11">
                                        <g transform="translate(0.5,0.5)">
                                            <rect
                                                x="536"
                                                y="972"
                                                width="231"
                                                height="148"
                                                rx="5.92"
                                                ry="5.92"
                                                :fill="fillColor"
                                                :stroke="strokeColor"
                                                stroke-width="2"
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
                                                                width: 229px;
                                                                height: 1px;
                                                                padding-top: 1046px;
                                                                margin-left: 537px;
                                                            ">
                                                            <div>
                                                                <div v-if="rows[2]" class="text-h3">
                                                                    <span
                                                                        :style="{
                                                                            color:
                                                                                hoveredOffset?.wcs === 2 &&
                                                                                hoveredOffset.axis === 0
                                                                                    ? primaryColor
                                                                                    : strokeColor,
                                                                        }">
                                                                        X {{ rows[2].X }}
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
                                                                        Y {{ rows[2].Y }}
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
                                                                        Z {{ rows[2].Z }}
                                                                    </span>
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
                                        v-model="aoffsetInput"
                                        :label="$t('Module5d.AoffsetPanel.Headline')"
                                        :suffix="'A'"
                                        :step="0.01"
                                        :current-pos="homingOffsets[0].toFixed(3)"
                                        @submit="sendOffset" />
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
        <tool-calibrate-dialog v-model="calibrateDialog" />
    </panel>
</template>

<script lang="ts">
import { Component, Mixins, Watch } from 'vue-property-decorator'
import BaseMixin from '@/components/mixins/base'
import Panel from '@/components/ui/Panel.vue'
import Responsive from '@/components/ui/Responsive.vue'
import WcsInput from '@/components/panels/Module5dControls/WcsInput.vue'
import ToolCalibrateDialog from '@/components/panels/Module5dControls/ToolCalibrateDialog.vue'
import { mdiChartLineVariant, mdiHome } from '@mdi/js'
import ThemeMixin from '@/components/mixins/theme'
import ControlMixin from '@/components/mixins/control'

@Component({
    components: {
        Panel,
        WcsInput,
        Responsive,
        ToolCalibrateDialog,
    },
})
export default class WcsGraph extends Mixins(BaseMixin, ControlMixin, ThemeMixin) {
    mdiChartLineVariant = mdiChartLineVariant
    mdiHome = mdiHome

    calibrateDialog = false
    get strokeColor() {
        return this.themeMode === 'dark' ? '#ffffff' : '#000000'
    }
    get fillColor() {
        return this.themeMode === 'dark' ? '#1E1E1E' : '#ffffff'
    }

    get primaryColor(): string {
        return this.$store.state.gui.uiSettings.primary
    }

    get wcsOffsets() {
        return this.$store.state.printer.module_5d.wcs_offsets ?? []
    }

    get homingOffsets() {
        return this.$store.state.printer.module_5d.homing_origin ?? []
    }

    @Watch('homingOffsets', { immediate: true, deep: true })
    updateHomingOffsets(newVal: number[]): void {
        this.aoffsetInput = newVal[0].toFixed(3)
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
            WCS: index,
            X: itm[0].toFixed(3),
            Y: itm[1].toFixed(3),
            Z: itm[2].toFixed(3),
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
