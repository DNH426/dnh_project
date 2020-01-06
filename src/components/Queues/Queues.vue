<template>
  <v-container>
    <v-col cols="12">
      <v-row :align="center" :justify="justify">
        <v-data-table
          :headers="headers"
          :items="queues"
          hide-default-footer
          class="elevation-1"
        ></v-data-table>
      </v-row>
    </v-col>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        { text: "Topic Name", value: "topicName" },
        { text: "DLQ Count", value: "dlqCount" },
        { text: "Read Timeout", value: "readTimeout" },
        { text: "Has Message", value: "hasMessage" },
        { text: "Alert Email Address", value: "alertEmail" },
        { text: "Self Publishing", value: "selfPublishing" }
      ],
      queues: [
        {
          topicName: "hrits.myhr.employee.updates.processing",
          dlqCount: 41663,
          readTimeout: 6000,
          hasMessage: "Yes",
          alertEmail: "kalapala@northwestern.edu",
          selfPublishing: "Allowed"
        },
        {
          topicName: "hrits.myhr.employee.updates",
          dlqCount: 210,
          readTimeout: 6000,
          hasMessage: "no",
          alertEmail: "kalapala@northwestern.edu",
          selfPublishing: "Denied"
        }
      ],
      alignment: "center",
      justify: "center"
    };
  }
};
</script>

<style>

</style>
