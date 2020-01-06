<template>
  <nav>
    <v-navigation-drawer v-model="drawer" dark="" app class="blue accent-2">
      <v-list>
        <v-list-item v-for="link in links" :key="link.text" router :to="link.route" active-class="border">
          <v-list-item-action>
            <v-icon>{{link.icon}}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{link.text}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data: () => ({
    drawer: true,
    links: [
      { icon: "fas fa-home", text: "Home", route: "/" },
      { icon: "fas fa-chart-line", text: "Queues", route: "/queues" },
      { icon: "fas fa-balance-scale-right", text: "Topics",route: "/topics"},
      { icon: "fas fa-briefcase", text: "Webhooks", route: "/webhooks" }
    ]
  })
};
</script>

<style scoped>
</style>