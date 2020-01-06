<template>
  <v-app>
    <NavBar />
    <v-content>
      <PageTitle />
      <Queues />
      <GoogleCharts />
    </v-content>
  </v-app>
</template>

<script>
import NavBar from "./components/TitleDrawer/NavBar"
import PageTitle from "./components/TitleDrawer/PageTitle";
import Queues from "./components/Queues/Queues";
import GoogleCharts from "./components/Queues/GoogleCharts";

export default {
  name: "App",

  components: {
    NavBar,
    PageTitle,
    Queues,
    GoogleCharts
  },

  data: () => ({
    //
  })
};
</script>
