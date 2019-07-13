<template>
    <div>
        <div>
            <button @click="calculateChartData">Calculate</button>
        </div>
        <chart1></chart1>
        <chart3 :chartData="chartData" :key="key"></chart3>
    </div>
</template>

<script>
    import chart1 from '../components/Chart1'
    import chart3 from '../components/Chart3'

    export default {
        components: {
            chart1,
            chart3
        },
        data() {
            return {
                chartData: null,
                key: 1,
                chartData1: {
                    datasets: [{
                        label: "Hot water temperature",
                        data: [
                            {x: 13.00, y: 32.25},
                            {x: 14.00, y: 33.20},
                            {x: 16.00, y: 34.10},
                            {x: 18.00, y: 35.00},
                            {x: 20.00, y: 35.85},
                            {x: 22.00, y: 36.65},
                            {x: 24.00, y: 37.50},
                            {x: 26.00, y: 38.25},
                            {x: 28.00, y: 39.00},
                            {x: 30.00, y: 39.70},
                            {x: 32.00, y: 40.40}
                        ],

                        showLine: true,
                        backgroundColor: [
                            'rgba(255, 99, 132, 0.2)'
                        ],
                        borderColor: [
                            'rgba(255,99,132,1)'
                        ],
                        borderWidth: 1
                    },
                        {
                            label: "Cooled water temperature",
                            data: [
                                {x: 12.00, y: 22.25},
                                {x: 14.00, y: 23.20},
                                {x: 16.00, y: 24.10},
                                {x: 18.00, y: 25.00},
                                {x: 20.00, y: 25.85},
                                {x: 22.00, y: 26.65},
                                {x: 24.00, y: 27.50},
                                {x: 26.00, y: 28.25},
                                {x: 28.00, y: 29.00},
                                {x: 30.00, y: 29.70},
                                {x: 32.00, y: 30.40}
                            ],

                            showLine: true,
                            backgroundColor: [
                                'rgba(0, 191, 255, 0.3)'
                            ],
                            borderColor: [
                                'rgba(0, 100, 255,1)'
                            ],
                            borderWidth: 1
                        },
                        {
                            label: "Wet bulb temperature",
                            data: [
                                {x: 12.00, y: 18},
                                {x: 14.00, y: 18},
                                {x: 16.00, y: 18},
                                {x: 18.00, y: 18},
                                {x: 20.00, y: 18},
                                {x: 22.00, y: 18},
                                {x: 24.00, y: 18},
                                {x: 26.00, y: 18},
                                {x: 28.00, y: 18},
                                {x: 30.00, y: 18},
                                {x: 32.00, y: 18}
                            ],

                            showLine: true,
                            backgroundColor: [
                                'rgba(126,211,33, 0.4)'
                            ],
                            borderColor: [
                                'rgba(81,135,21,1)'
                            ],
                            borderWidth: 1
                        }]
                }
            }
        },
        methods: {
            calculateChartData() {
                this.chartData = this.chartData1
                this.key +=1

            }
        }
    }
</script>

<style>

</style>