<template>
  <div>
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
    <bar-chart></bar-chart>
  </div>
</template>

<script>
import MainNavbar from "../MainNavbar.vue";
import Widgets from "../Widgets.vue";
import BarChart from "../BarChart.vue";

export default {
  components: {
    MainNavbar,
    Widgets,
    BarChart,
  },
};
</script>
