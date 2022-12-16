<template>
  <v-card class="mt-5 rounded-lg" width="100%" color="grey lighten-4">
    <v-tabs v-model="tab" color="black" background-color="grey lighten-4">
      <v-tabs-slider color="deep-purple accent-2"></v-tabs-slider>

      <v-tab href="#tab-1"> Summary </v-tab>

      <v-tab href="#tab-2"> Table </v-tab>

      <v-tab href="#tab-3"> Charts </v-tab>

      <v-tab href="#tab-4"> Reporting </v-tab>

      <v-tab href="#tab-5"> Charts </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab" class="grey lighten-4">
      <v-tab-item v-for="i in 5" :key="i" :value="'tab-' + i" class="mb-5">
        <v-card color="grey lighten-4" flat>
          <v-card-text>{{ info }}</v-card-text>

          <v-card
            color="white"
            outlined
            class="mt-2 mb-2 mr-8 ml-8"
            elevation="2"
          ><v-row>
            <v-col cols="1">
            <v-icon large color="orange" class="mt-1 mb-1 ml-3 mr-3"
              >mdi-bitcoin</v-icon
            >
            </v-col>
            <v-card-title>Bitcoin</v-card-title><v-spacer></v-spacer><v-btn depressed class="ml-2 mr-2 mt-4 mb-1">Sell</v-btn> <v-btn depressed class="ml-2 mr-5 mt-4 mb-1 deep-purple accent-2 white--text">Buy</v-btn> 
            </v-row>
          </v-card>
          <v-card
            color="white"
            outlined
            class="mt-2 mb-2 mr-8 ml-8"
            elevation="2"
          ><v-row>
            <v-col cols="1">
            <v-icon large color="black" class="mt-1 mb-1 ml-3 mr-3"
              >mdi-ethereum</v-icon
            >
            </v-col>
            <v-card-title>Ethereum</v-card-title><v-spacer></v-spacer><v-btn depressed class="ml-2 mr-2 mt-4 mb-1">Sell</v-btn> <v-btn depressed class="ml-2 mr-5 mt-4 mb-1 deep-purple accent-2 white--text">Buy</v-btn>
            </v-row>
          </v-card>
          <v-card
            color="white"
            outlined
            class="mt-2  mr-8 ml-8"
            elevation="2"
          >
            <v-icon large color="black" class="mt-1 mb-1 ml-3 mr-3"
              ></v-icon
            >
          </v-card>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      info: null,
      tab: null,
    };
  },
  methods: {
    async getData() {
      try {
        let response = await fetch(
          "https://coinmarketcap.com/v1/cryptocurrency/listings/latest",
          {
            "X-CMC_PRO_API_KEY": "98d2e57e-fc0c-4354-8078-57c0aeda360a",
            Accepts: "application/json",
          }
        )
          .then((response) => response.json())
          .then((jsondata) => console.log(jsondata));
        console.log(response);
        this.info = await response;
      } catch (error) {
        console.log(error);
      }
    },
  },
  created() {
    this.getData();
  },
};
</script>

<style>
</style>