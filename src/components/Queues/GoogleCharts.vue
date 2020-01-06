<template>
  <v-app>
    <v-container>
      <v-col cols="12" md="12">
        <template>
          <div id="app">
            <h1 class="headline mb-2 grey--text">Pending Messages in Queue</h1>
            <GChart type="ColumnChart" :data="pending" :options="chartOptions" />

            <h1 class="headline mb-2 grey--text">Expired Messages</h1>
            <GChart type="ColumnChart" :data="time" :options="chartOptions" />

            <h1 class="headline mb-2 grey--text">Acknowledged Messages</h1>
            <GChart type="ColumnChart" :data="acknowledged" :options="chartOptions" />

            <h1 class="headline mb-2 grey--text">Time of Message in Queue (ms)</h1>
            <GChart type="ColumnChart" :data="time" :options="chartOptions" />
          </div>
        </template>
      </v-col>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    pending: [
      ["Year", "A", "B", "C"],
      ["2014", 1000, 2000, 3000]
    ],
    expired: [
      ["Year", "A", "B", "C"],
      ["2015", 500, 750, 1000]
    ],
    acknowledged: [
      ["Year", "A", "B", "C"],
      ["2016", 100, 200, 300]
    ],
    time: [
      ["Year", "A", "B", "C"], 
      ["2017", 2500, 3000, 1500]
      ],
    chartOptions: {
      chart: {
        title: "Company Performance",
        subtitle: "Sales, Expenses, and Profit: 2014-2017"
      }
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
.container {
  background: #ffff;
}
</style>