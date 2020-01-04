<template>
  <v-container>
    <v-col cols="12">
      <v-row :align="center" :justify="justify">
        <h1>Eventhub Dashboard Title Container</h1>
      </v-row>
    </v-col>
  </v-container>
</template>

<script>
export default {
    data() {
    return {
      alignment: "center",
      justify: "center"
    };
  }
};
</script>

<style></style>
