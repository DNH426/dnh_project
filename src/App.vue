<template>
  <v-app>
    <v-app-bar app color="primary" dark> </v-app-bar>
    <v-content>
      <PageTitle />
      <Queues />
      <GoogleCharts />
    </v-content>
  </v-app>
</template>

<script>
import PageTitle from "./components/TitleDrawer/PageTitle";
import Queues from "./components/Queues/Queues";
import GoogleCharts from "./components/Queues/GoogleCharts";

export default {
  name: "App",

  components: {
    PageTitle,
    Queues,
    GoogleCharts
  },

  data: () => ({
    //
  })
};
</script>
