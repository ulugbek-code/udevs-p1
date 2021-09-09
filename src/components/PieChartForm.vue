<script>
// Import the base chart
import { Doughnut } from "vue-chartjs";

// Extend it
export default {
  extends: Doughnut,
  props: ["chartData", "options"],
  mounted() {
    // Overwriting base render method with actual data.
    this.renderChart(this.chartData, this.options);
  },
};
</script>
