<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <TopCards />
      </v-col>
      <v-col cols="4">
        <LineChart />
      </v-col>
      <v-col cols="4">
        <PieChart />
      </v-col>
      <v-col cols="4">
        <DonutChart />
      </v-col>
      <v-col cols="6">
        <v-row>
          <v-col cols="12">
            <GuageChart />
          </v-col>
          <v-col cols="12">
            <ListComponent />
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="6">
        <v-row>
          <v-col cols="12">
            <DataTableComponent />
          </v-col>
          <v-col cols="12">
            <DataTableComponent />
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// import TopCards from "~/components/TopCards.vue";
// import ChartComponent from "~/components/ChartComponent.vue";
// import DataTableComponent from "~/components/DataTableComponent.vue";
// import ListComponent from "~/components/ListComponent.vue";

export default {
  components: {
    // TopCards,
    // ChartComponent,
    // DataTableComponent,
    // ListComponent,
  },
};
</script>
