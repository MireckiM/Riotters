<template>
  <v-app>
    <v-main>
      <Main />
    </v-main>
  </v-app>
</template>

<script>
import Main from "./components/Main";

export default {
  name: "App",

  components: {
    Main,
    //HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
#app {
  background-color: rgb(26, 26, 26);
}
</style>
