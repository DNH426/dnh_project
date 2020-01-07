<template>
  <v-app>
    <div id="app">
      <v-row class="space">
        <v-col cols="12" sm="6">
          <div class="my-2">
            <v-card>
              <h1 class="headline mb-2 grey--text">Pending</h1>
              <GChart type="ColumnChart" :data="pending" :options="chartOptions" />
            </v-card>
          </div>
        </v-col>
        <v-col cols="12" sm="6">
          <div class="my-2">
            <v-card>
              <h1 class="headline mb-2 grey--text">Expired</h1>
              <GChart type="ColumnChart" :data="expired" :options="chartOptions" />
            </v-card>
          </div>
        </v-col>
      </v-row>
      <v-row class="space">
        <v-col cols="12" sm="6">
          <div class="my-2">
            <v-card>
              <h1 class="headline mb-2 grey--text">Acknowledged</h1>
              <GChart type="ColumnChart" :data="acknowledged" :options="chartOptions" />
            </v-card>
          </div>
        </v-col>
        <v-col cols="12" sm="6">
          <div class="my-2">
            <v-card>
              <h1 class="headline mb-2 grey--text">Time</h1>
              <GChart type="ColumnChart" :data="time" :options="chartOptions" />
            </v-card>
          </div>
        </v-col>
      </v-row>
    </div>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    pending: [["Year", "A", "B", "C"], ["2014", 1000, 2000, 3000]],
    expired: [["Year", "A", "B", "C"], ["2015", 500, 750, 1000]],
    acknowledged: [["Year", "A", "B", "C"], ["2016", 100, 200, 300]],
    time: [["Year", "A", "B", "C"], ["2017", 2500, 3000, 1500]],
    chartOptions: {
      chart: {
        title: "Company Performance",
        subtitle: "Sales, Expenses, and Profit: 2014-2017"
      },
      colors: ["#9032d9", "#492a78", "#7570b3"],
      width: "880px"
    }
  }),
  name: "App",
  components: {},
  computed: {
    theme() {
      return this.$vuetify.theme.dark ? "dark" : "light";
    }
  }
};
</script>

<style>
.space {
  padding: 5px !important;
}
</style>