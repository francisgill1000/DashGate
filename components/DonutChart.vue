<template>
  <v-card style="min-height: 300px;" elevation="5">
    <v-card-title>Apex Chart</v-card-title>
    <v-card-text>
      <ApexChart :options="options" :series="series" type="donut" />
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      series: [44, 55, 41, 17, 15],
      options: {
        chart: {
          type: "donut",
        },
        responsive: [
          {
            breakpoint: 480,
            options: {
              chart: {
                width: 200,
              },
              legend: {
                position: "bottom",
              },
            },
          },
        ],
      },
    };
  },
};
</script>
