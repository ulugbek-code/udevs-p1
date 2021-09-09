<script>
// Import the base chart
import { Bar } from "vue-chartjs";

// Extend it
export default {
  extends: Bar,
  mounted() {
    // Overwriting base render method with actual data.
    this.renderChart(
      {
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
            backgroundColor: "#F6785D",
            data: [3, 7, 4, 3, 2, 7, 4, 3, 9, 6],
          },
          {
            label: "кутаётганлар",
            backgroundColor: "#D86CF7",
            data: [4, 3, 5, 8, 3, 2, 7, 4, 6, 4],
          },
          {
            label: "хизмат кўрсатилганлар",
            backgroundColor: "#57F875",
            data: [7, 2, 6, 12, 3, 5, 8, 7, 4, 7],
          },
        ],
      },
      {
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
      }
    );
  },
};
</script>
