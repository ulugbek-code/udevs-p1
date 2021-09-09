<script>
// Import the base chart
import { Doughnut } from "vue-chartjs";

// Extend it
export default {
  extends: Doughnut,
  mounted() {
    // Overwriting base render method with actual data.
    this.renderChart({
      labels: ["ўлим", "никоҳ", "туғилиш", "ажрим"],
      datasets: [
        {
          label: "Population (millions)",
          backgroundColor: [
            "#3e95cd",
            "#8e5ea2",
            "#3cba9f",
            "#e8c3b9",
            "#c45850",
          ],
          data: [3124, 1523, 9213, 1231],
        },
      ],
    });
  },
};
</script>
