<template>
  <v-card class="rounded-lg grey lighten-4" flat>
    <v-card-title class="text-h6 mb-1">
      Summary <v-spacer></v-spacer
      ><v-icon color="grey darken-1">mdi-dots-horizontal</v-icon></v-card-title
    >

    <v-card-actions>
      <v-btn fab flat depressed class="mb-2 mt-10">
        <v-icon small color="deep-purple accent-2" class=""
          >mdi-circle-medium</v-icon
        >
      </v-btn>
      <p class="mt-13 grey--text caption">This month</p>
      <v-btn fab flat depressed class="mb-2 mt-10">
        <v-icon small color="grey lighten-1" class=""
          >mdi-circle-medium</v-icon
        >
      </v-btn>
      <p class="mt-13 grey--text caption">Last month</p>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {};
</script>

<style>
</style>