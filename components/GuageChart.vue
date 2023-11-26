<template>
  <v-card style="min-height: 300px;" elevation="5">
    <v-card-title>Apex Chart</v-card-title>
    <v-card-text>
      <ApexChart :options="options" :series="series" type="radialBar" />
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      series: [67],
      options: {
        chart: {
          height: 350,
          type: "radialBar",
          offsetY: -10,
        },
        plotOptions: {
          radialBar: {
            startAngle: -135,
            endAngle: 135,
            dataLabels: {
              name: {
                fontSize: "16px",
                color: undefined,
                offsetY: 120,
              },
              value: {
                offsetY: 76,
                fontSize: "22px",
                color: undefined,
                formatter: function (val) {
                  return val + "%";
                },
              },
            },
          },
        },
        fill: {
          type: "gradient",
          gradient: {
            shade: "dark",
            shadeIntensity: 0.15,
            inverseColors: false,
            opacityFrom: 1,
            opacityTo: 1,
            stops: [0, 50, 65, 91],
          },
        },
        stroke: {
          dashArray: 4,
        },
        labels: ["Label"],
      },
    };
  },
};
</script>
