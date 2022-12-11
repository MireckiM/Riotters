<template>
  <v-container>
    <v-card class="py-12" outlined>
      <v-content class="my-6">
        <v-row
          ><v-col cols="1"></v-col
          ><v-row
            >
              <v-text-field
                hide-details
                filled
                flat
                dense
                label="Search"
                prepend-inner-icon="mdi-magnify"
              ></v-text-field>

              <v-spacer></v-spacer>
              <v-btn class="mr-2" height="55px" depressed>
                <v-icon color="grey">mdi-bell-ring-outline</v-icon>
              </v-btn>

              <v-btn class="ml-2" height="55px" depressed>
                <v-icon color="grey">mdi-format-list-bulleted</v-icon>
              </v-btn> </v-row
          ><v-col cols="1"></v-col>
        </v-row>
      </v-content>
    </v-card>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
.v-text-field {
  max-width: 200px;
}
</style>