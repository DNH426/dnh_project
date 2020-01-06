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
import NavBar from "./components/TitleDrawer/NavBar";
import PageTitle from "./components/TitleDrawer/PageTitle";
import Queues from "./components/Queues/Queues";
import GoogleCharts from "./components/Queues/GoogleCharts";
// import Topics from "./components/Topics/Topics"

export default {
  name: "App",

  components: {
    NavBar,
    PageTitle,
    Queues,
    GoogleCharts
    // Topics,
  },

  data: () => ({
    //
  })
};
</script>

<style>
body {
  background: #ffff;
}

.v-application--wrap {
  min-height: 100%;
}
</style>