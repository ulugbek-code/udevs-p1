<template>
  <div id="charts-wrapper">
    <div class="wrapper">
      <div class="bar">
        <bar-chart :title="barChartTitle"></bar-chart>
      </div>
      <div class="pie">
        <pie-chart :title="pieChartTitle"></pie-chart>
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
  props: ["bar-chart-title", "pie-chart-title"],
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
.pie {
  width: 29%;
}
</style>
