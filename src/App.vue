<template>
  <div id="app">
    <dashboard></dashboard>
  </div>
</template>

<script>
import Dashboard from "./components/pages/Dashboard.vue";

export default {
  name: "App",
  components: {
    Dashboard,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "Inter", sans-serif;
  background: mediumaquamarine;
}
/* #app {
  /* margin-left: 320px; */
</style>
