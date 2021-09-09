<template>
  <div id="pie-chart-container">
    <div class="wrapper">
      <h2>{{ title }}</h2>
      <div class="canvas">
        <div class="population">
          <h3>{{ population }}</h3>
          <p>Aholi</p>
        </div>
        <pie-chart-form
          :chart-data="pieChartData"
          :options="options"
          :styles="myStyles"
        ></pie-chart-form>
      </div>
    </div>
  </div>
</template>

<script>
import PieChartForm from "./PieChartForm.vue";

export default {
  props: ["title", "pie-chart-data", "options", "population"],
  components: { PieChartForm },
  computed: {
    myStyles() {
      return {
        height: "480px",
        position: "relative",
      };
    },
  },
};
</script>

<style scoped>
#pie-chart-container {
  width: 100%;
  height: 600px;
  padding-bottom: 30px;
  background: rgba(247, 247, 249, 1);
}
.wrapper {
  width: 100%;
  height: 100%;
  margin: 0 auto;
  background: #fff;
  padding: 20px;
  border-radius: 16px;
}
.wrapper h2 {
  font-size: 24px;
}
.canvas {
  width: 100%;
  height: 485px;
  margin-top: 1rem;
  position: relative;
}
.population {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 100;
  text-align: center;
}
.population h3 {
  font-weight: 700;
  font-size: 32px;
}
.population p {
  font-size: 18px;
}
</style>
