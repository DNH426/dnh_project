<template>
  <v-container id="dropdown">
    <v-row :align="center" :justify="justify">
      <v-col justify="center" cols="4" sm="4">
        <div class="text-center">
          <h1 class="display-2">Eventhub Dashboard</h1>
          <h4>Please select your Team and Application</h4>
          <br/>
          <v-menu offset-y>
            <template v-slot:activator="{ on }">
              <v-btn class="btn" color="#492a78" dark v-on="on">Integration Team</v-btn>
            </template>
            <v-list>
              <v-list-item v-for="(item, index) in items" :key="index">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>
        <br />
        <div class="text-center">
          <v-menu offset-y>
            <template v-slot:activator="{ on }">
              <v-btn class="btn" color="#492a78" dark v-on="on">Sailpoint Integration Application</v-btn>
            </template>
            <v-list>
              <v-list-item v-for="(item, index) in items" :key="index">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>
      </v-col>
    </v-row>
          <v-divider class="my-3"></v-divider>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: "Click Me" },
      { title: "Click Me" },
      { title: "Click Me" },
      { title: "Click Me 2" }
    ],
    alignment: "center",
    justify: "center"
  })
};
</script>

<style>
.my-3 {
  margin-left: 10%;
  margin-right: 10%;
}

.btn {
  width: 100%;
  min-width: 100%;
}
</style>