<template>
  <div id="charts-wrapper">
    <div class="wrapper">
      <div :class="!isFxdyo ? 'full' : ''" class="bar">
        <bar-chart
          :chart-data="chartData"
          :bar-options="barOptions"
          :title="barChartTitle"
        ></bar-chart>
      </div>
      <div v-if="isFxdyo" class="pie">
        <pie-chart
          :pie-chart-data="pieChartData"
          :options="options"
          :population="population"
          :title="pieChartTitle"
        ></pie-chart>
      </div>
    </div>
  </div>
</template>

<script>
import BarChart from "./BarChart.vue";
import PieChart from "./PieChart.vue";

export default {
  components: {
    BarChart,
    PieChart,
  },
  props: [
    "bar-chart-title",
    "chart-data",
    "bar-options",
    "pie-chart-title",
    "is-fxdyo",
    "pie-chart-data",
    "options",
    "population",
  ],
};
</script>

<style scoped>
#charts-wrapper {
  width: 100%;
  background: rgba(247, 247, 249, 1);
}
.wrapper {
  width: 90%;
  height: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
.bar {
  width: 69%;
}
.bar.full {
  width: 100%;
}
.pie {
  width: 29%;
}
</style>
