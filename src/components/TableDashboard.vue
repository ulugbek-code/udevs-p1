<template>
  <div id="table-dashboard-container">
    <div class="table-wrapper">
      <h2>{{ tableTitle }}</h2>
      <table class="bordered">
        <tr>
          <th v-for="(t, i) in tableHeader" :key="i">{{ t }}</th>
        </tr>
        <tr v-for="(t, i) in tableData" :key="i">
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
  props: ["table-title", "table-header", "table-data"],
};
</script>

<style scoped>
#table-dashboard-container {
  width: 100%;
  /* height: 824px;  */
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
  margin-top: 1.2rem;
  border-collapse: separate;
  border-spacing: 0px;
  width: 100%;
}
.bordered {
  border-radius: 16px;
  border: 1px solid rgb(232, 241, 247);
}
th {
  font-size: 14px;
  text-transform: uppercase;
  background: linear-gradient(
    180deg,
    rgba(229, 233, 235, 0.25) 0%,
    #e5e9eb 100%
  );
}
th:first-child {
  border-top-left-radius: 16px;
}
th:last-child {
  border-top-right-radius: 16px;
}
td,
th {
  border-bottom: 1px solid #dddddd;
  text-align: left;
  padding: 16px;
}
td {
  font-size: 18px;
}
tr:nth-child(odd) {
  background-color: rgba(246, 248, 249, 1);
}
tr:last-child td:first-child {
  /* border-bottom: none; */
  border-bottom-left-radius: 16px;
}
tr:last-child td:last-child {
  /* border-bottom: none; */
  border-bottom-right-radius: 16px;
}
</style>
