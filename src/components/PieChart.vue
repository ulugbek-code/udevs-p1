<template>
  <div id="pie-chart-container">
    <div class="wrapper">
      <h2>{{ title }}</h2>
      <div class="canvas">
        <!-- Will be deleted -->
        <h1>For Pie Chart</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title"],
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
  background: rgb(179, 92, 92);
  margin-top: 1rem;
  /* will be deleted */
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
