<template>
  <div id="table-dashboard-container">
    <div class="table-wrapper">
      <h2>{{ tableTitle }}</h2>
      <table>
        <tr>
          <th v-for="t in tableHeader" :key="t">{{ t }}</th>
        </tr>
        <tr v-for="t in tableData" :key="t">
          <td>{{ t.branches }}</td>
          <td>{{ t.numberOfVisits }} ({{ t.numberOfVisitorsPerscentage }}%)</td>
          <td>{{ t.employees }}({{ t.employeesPercentage }})</td>
          <td>{{ t.averageVisits }}</td>
          <td>{{ t.averageWaitingTime }}</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  props: ["table-title"],
  data() {
    return {
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
#table-dashboard-container {
  width: 100%;
  height: 824px;
  padding-bottom: 30px;
  background: rgba(247, 247, 249, 1);
}
.table-wrapper {
  width: 90%;
  height: 100%;
  overflow-y: auto;
  margin: 0 auto;
  padding: 20px;
  border-radius: 16px;
  background: #fff;
}
table {
  width: 100%;
  margin-top: 20px;
  border-collapse: collapse;
}
th {
  background: linear-gradient(
    180deg,
    rgba(229, 233, 235, 0.7) 0%,
    #e5e9eb 100%
  );
  /* padding: 16px 32px; */
}
tr,
td {
  position: relative;
  text-align: left;
}
</style>
