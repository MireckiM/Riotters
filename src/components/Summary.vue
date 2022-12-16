<template>
  <v-card class="rounded-lg grey lighten-4" flat height="100%">
    <v-card-title class="text-h6 mb-1">
      Summary <v-spacer></v-spacer
      ><v-icon color="grey darken-1">mdi-dots-horizontal</v-icon></v-card-title
    >
    <v-sheet
      class="v-sheet--offset"
      color="grey lighten-4"
      max-width="calc(100% - 16px)"
      
    >
      <v-sparkline
        :value="value"
        fill
        line-width="7"
        auto-draw
        :gradient="gradient"
        smooth="30"
        height="120px"
      ></v-sparkline>
    </v-sheet>
    <v-card-actions>
      <v-btn fab depressed class="mb-2 mt-10">
        <v-icon small color="deep-purple accent-2" class=""
          >mdi-circle-medium</v-icon
        >
      </v-btn>
      <p class="mt-13 grey--text caption">This month</p>
      <v-btn fab depressed class="mb-2 mt-10">
        <v-icon small color="grey lighten-1" class="">mdi-circle-medium</v-icon>
      </v-btn>
      <p class="mt-13 grey--text caption">Last month</p>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    gradient: ["indigo", "white"],
    value: [0, 2, 5, 4, 9, 5, 10, 9],
  }),
};
</script>

<style>
</style>