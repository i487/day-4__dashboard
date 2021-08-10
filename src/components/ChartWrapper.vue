<template>
    <section class="chart">
        <h3 class="chart__title">Hospital Surver</h3>
        <Area-chart />
    </section>
</template>

<script>
import AreaChart from './AreaChart.vue'
export default {
  components: { AreaChart },
    name: "ChartWrapper",
    data () {
        return {
            chartData: {
                Books: 24,
                Magazine: 30,
                Newspapers: 10
            }
        }
    }
}
</script>

<style lang="scss">
.chart {
    padding: 24px;
    background: white;
    margin-top: 24px;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
}
</style>