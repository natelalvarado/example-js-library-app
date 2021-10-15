<template>
  <chartxkcd-line :config="config"></chartxkcd-line>
</template>

<script>
import { chartXKCDLine } from "chart.xkcd-vue";

export default {
  name: "app",
  data() {
    return {
      config: {
        title: "My Confidence During Coding Bootcamp",
        xLabel: "Week",
        yLabel: "Confidence",
        data: {
          labels: ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10"],
          datasets: [
            {
              label: "Confidence",
              data: [50, 10, 20, 30, 40, 90, 75, 10, 50, 50],
            },
          ],
        },
      },
    };
  },
  components: {
    "chartxkcd-line": chartXKCDLine,
  },
};
</script>
