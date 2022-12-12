<template>
  <v-card class="mt-5 rounded-lg" width="100%">
    <v-tabs v-model="tab" color="black" background-color="grey lighten-4">
      <v-tabs-slider color="deep-purple accent-2"></v-tabs-slider>

      <v-tab href="#tab-1"> Summary </v-tab>

      <v-tab href="#tab-2"> Table </v-tab>

      <v-tab href="#tab-3"> Charts </v-tab>

      <v-tab href="#tab-4"> Reporting </v-tab>

      <v-tab href="#tab-5"> Charts </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="i in 5" :key="i" :value="'tab-' + i">
        <v-card color="grey lighten-4" flat>
          <v-card-text>data</v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      tab: null,
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
    };
  },
};
</script>

<style>
</style>