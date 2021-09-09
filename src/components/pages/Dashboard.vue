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
      <bar-chart
        :chart-data="barChartData"
        :bar-options="barOptions"
        title="Ҳудудлар бўйича ташрифлар"
      ></bar-chart>
    </div>
    <charts-wrapper
      bar-chart-title="Ҳафталик статистика"
      :chart-data="barChartData"
      :bar-options="barOptions"
      pie-chart-title="ФҲДЁ хизматлари бўйича"
      :pie-chart-data="pieChartData"
      :options="pieChartOptions"
      :is-fxdyo="isFxdyo"
    ></charts-wrapper>
    <table-dashboard
      table-title="Филиаллар буйича статистика"
      :table-header="tableHeader"
      :table-data="tableData"
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
  data() {
    return {
      isFxdyo: true,
      barChartData: {
        labels: [
          "Тошкент ш.",
          "Тошкент в.",
          "Сирдарё",
          "Жиззах",
          "Самарқанд",
          "Сурхандарё",
          "Қашқадарё",
          "Бухоро",
          "Хоразм",
          "Қорақалпоғистон",
        ],
        datasets: [
          {
            label: "кўп кутганлар",
            backgroundColor: "#F82C2C",
            data: [3, 7, 4, 3, 2, 7, 4, 3, 9, 6],
          },
          {
            label: "кутаётганлар",
            backgroundColor: "#C82BF4",
            data: [4, 3, 5, 8, 3, 2, 7, 4, 6, 4],
          },
          {
            label: "хизмат кўрсатилганлар",
            backgroundColor: "#15F23F",
            data: [7, 2, 6, 12, 3, 5, 8, 7, 4, 7],
          },
        ],
      },
      barOptions: {
        scales: {
          yAxes: [
            {
              ticks: {
                beginAtZero: true,
              },
              gridLines: {
                display: true,
              },
            },
          ],
          xAxes: [
            {
              gridLines: {
                display: false,
              },
            },
          ],
        },
        legend: {
          display: true,
        },
        responsive: true,
        maintainAspectRatio: false,
      },
      pieChartData: {
        labels: ["ўлим", "никоҳ", "туғилиш", "ажрим"],
        datasets: [
          {
            label: "Population (millions)",
            backgroundColor: ["#EE4F4F", "#2BD838", "#4080F4", "#B733F3"],
            data: [3124, 1523, 9213, 1231],
          },
        ],
      },
      pieChartOptions: {
        responsive: true,
        maintainAspectRatio: false,
      },
      tableHeader: [
        "филиаллар",
        "ташрифлар сони",
        "ходимлар сони",
        "кунлик ўртача ташрифлар",
        "ўртаcа кутиш вақти",
      ],
      tableData: [
        {
          branches: "Яшнобод тумани ДХМ",
          numberOfVisits: 4846,
          numberOfVisitorsPerscentage: 12,
          employees: 1234,
          employeesPercentage: 42,
          averageVisits: 429,
          averageWaitingTime: 426,
        },
        {
          branches: "Яшнобод тумани ДХМ",
          numberOfVisits: 4846,
          numberOfVisitorsPerscentage: 12,
          employees: 1234,
          employeesPercentage: 42,
          averageVisits: 429,
          averageWaitingTime: 426,
        },
        {
          branches: "Яшнобод тумани ДХМ",
          numberOfVisits: 4846,
          numberOfVisitorsPerscentage: 12,
          employees: 1234,
          employeesPercentage: 42,
          averageVisits: 429,
          averageWaitingTime: 426,
        },
        {
          branches: "Яшнобод тумани ДХМ",
          numberOfVisits: 4846,
          numberOfVisitorsPerscentage: 12,
          employees: 1234,
          employeesPercentage: 42,
          averageVisits: 429,
          averageWaitingTime: 426,
        },
        {
          branches: "Яшнобод тумани ДХМ",
          numberOfVisits: 4846,
          numberOfVisitorsPerscentage: 12,
          employees: 1234,
          employeesPercentage: 42,
          averageVisits: 429,
          averageWaitingTime: 426,
        },
      ],
    };
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
