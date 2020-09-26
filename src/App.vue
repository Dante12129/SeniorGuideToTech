<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <h1>Senior Guide To Tech</h1>
    </v-app-bar>

    <v-main>
      <Main />
    </v-main>

    <MainNavigation app />
  </v-app>
</template>

<script>

import Main from "@/components/Main";
import MainNavigation from "@/components/MainNavigation";
export default {
  name: 'App',

  components: {
    MainNavigation,
    Main
  },

  data: () => ({
    //
  }),

  created() {
    this.$vuetify.theme.dark = true
  }
};
</script>
