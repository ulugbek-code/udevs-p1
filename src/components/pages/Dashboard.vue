<template>
  <div id="dashboard">
    <main-navbar></main-navbar>
    <widgets
      visits="29,000"
      queue="12,345"
      awaited="12,345"
      finished="12,340"
      queuePer="48"
      awaitedPer="32"
      finishedPer="24"
    ></widgets>
    <div class="wrapper">
      <bar-chart title="Ҳудудлар бўйича ташрифлар"></bar-chart>
    </div>
    <charts-wrapper
      bar-chart-title="Ҳафталик статистика"
      pie-chart-title="ФҲДЁ хизматлари бўйича"
    ></charts-wrapper>
    <table-dashboard
      table-title="Филиаллар буйича статистика"
    ></table-dashboard>
  </div>
</template>

<script>
import MainNavbar from "../MainNavbar.vue";
import Widgets from "../Widgets.vue";
import BarChart from "../BarChart.vue";
import ChartsWrapper from "../ChartsWrapper.vue";
import TableDashboard from "../TableDashboard.vue";

export default {
  components: {
    MainNavbar,
    Widgets,
    BarChart,
    ChartsWrapper,
    TableDashboard,
  },
};
</script>

<style scoped>
#dashboard {
  background: rgba(247, 247, 249, 1);
}
.wrapper {
  width: 90%;
  margin: 0 auto;
  /* background: rgb(93, 93, 199); */
}
</style>
