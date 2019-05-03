<template>
    <div>
        <h1>About</h1>
        <Bar />
    </div>
</template>

<script>
    import {Bar} from 'vue-chartjs'

    export default {
        extends: Bar,
        mounted(){
            this.renderChart(this.chartdata, this.options)
        },
        data() {
            return {
                chartdata: {
                    datacollection: {
                        labels: ['January', 'February'],
                        datasets: [
                            {
                                label: 'Data One',
                                backgroundColor: '#f87979',
                                data: [40, 20]
                            }
                        ]
                    }
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false
                }
            }
        },
        comments: {
            Bar
        }
    }
</script>

<style>

</style>
