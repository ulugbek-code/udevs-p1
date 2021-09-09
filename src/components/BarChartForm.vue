<script>
// Import the base chart
import { Bar } from "vue-chartjs";

// Extend it
export default {
  extends: Bar,
  props: ["chart-data", "options"],
  mounted() {
    // Overwriting base render method with actual data.
    this.renderChart(this.chartData, this.options);
  },
};
</script>
