<template>
  <v-jumbotron color="grey lighten-4">
    <v-container>
      <v-col cols="12">
        <v-row :align="center" :justify="justify">
          <v-layout align-center>
            <v-flex>
              <h3 class="display-3">Eventhub Dashboard</h3>
              <v-divider class="my-3"></v-divider>
              <v-btn large color="primary" class="mx-0">Select Company</v-btn>
            </v-flex>
          </v-layout>
        </v-row>
      </v-col>
      </v-container>
  </v-jumbotron>
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
