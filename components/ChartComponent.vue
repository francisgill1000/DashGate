<template>
  <v-card>
    <v-card-title>Apex Chart</v-card-title>
    <v-card-text>
      <ApexChart :options="options" :series="series" type="line" />
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      options: {
        chart: {
          id: "myChart",
        },
        xaxis: {
          categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998],
          labels: {
            style: {
              fontSize: '12px', // Adjust the font size or other styles as needed
            },
          },
        },
        yaxis: {
          labels: {
            style: {
              fontSize: '12px', // Adjust the font size or other styles as needed
            },
          },
        },
      },
      series: [
        {
          name: "series-1",
          data: [30, 40, 45, 50, 49, 60, 70, 91],
        },
      ],
    };
  },
};
</script>
