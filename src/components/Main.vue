<template>
  <v-container>
    <v-card class="py-12 rounded-xl" outlined>
      <v-content class="my-6">
        <v-row
          ><v-col cols="1"></v-col
          ><v-col>
            <v-row>
              <v-text-field
                class="ml-3"
                hide-details
                filled
                flat
                dense
                label="Search"
                prepend-inner-icon="mdi-magnify"
              ></v-text-field>

              <v-spacer></v-spacer>
              <v-badge
                bordered
                color="error"
                overlap
                offset-x="20"
                offset-y="10"
              >
                <v-btn class="mr-2 grey lighten-4" height="55px" depressed>
                  <v-icon color="grey darken-1">mdi-bell-ring-outline</v-icon>
                </v-btn></v-badge
              >

              <v-btn class="ml-2 mr-3 grey lighten-4" height="55px" depressed>
                <v-icon color="grey darken-1">mdi-format-list-bulleted</v-icon>
              </v-btn> </v-row
            ><v-row class="b"
              ><v-col><Balance /></v-col
              ><v-col class="hidden-sm-and-down"><Summary /></v-col></v-row
            ><v-row
              ><v-col><Tabs /></v-col></v-row
            ><v-col class="hidden-md-and-up"><Summary /></v-col
            ><v-row></v-row> </v-col
          ><v-col cols="1"></v-col
        ></v-row>
      </v-content>
    </v-card>
  </v-container>
</template>

<script>
import Balance from "./Balance";
import Summary from "./Summary";
import Tabs from "./Tabs";

export default {
  name: "Main",

  components: {
    Balance,
    Summary,
    Tabs,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
.v-text-field {
  max-width: 200px;
}
/*#red {
  background-color: aquamarine;
}
#blue {
  background-color: aqua;
}*/
</style>