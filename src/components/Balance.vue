<template>
  <v-card class="rounded-lg grey lighten-4" flat height="100%">
    <v-card-title class="text-h6 mb-1">
      Current Balance <v-spacer></v-spacer
      ><v-icon color="grey darken-1">mdi-dots-horizontal</v-icon></v-card-title
    >
    <p class="text-h4 ml-3">
      <v-icon x-large color="grey darken-1" class="mb-2"
        >mdi-currency-usd</v-icon
      >21432.23
    </p>
    <p class="text-h7 mb-6 ml-6 green--text font-weight-medium">
      <v-icon small color="green" class="mb-1 mr-1"
        >mdi-arrow-top-right-thin-circle-outline</v-icon
      >12% vs last month
    </p>

    <v-card-actions class="font-weight-normal ml-4">
      <v-btn color="deep-purple accent-2" dark depressed class="mb-5 mt-15">
        Quick Invest
      </v-btn>
      <v-btn class="deep-purple--text mb-5 mt-15" color="white" dark depressed>
        Show Report
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {};
</script>

<style>
.v-btn {
  font-size: x-small !important;
}
</style>