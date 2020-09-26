<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <h1>Senior Guide To Tech</h1>
    </v-app-bar>

    <v-main>
      <Main :text="text" />
    </v-main>

    <MainNavigation @update:selected="text = $event" />
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
    text: 'Nothing selected yet'
  }),

  created() {
    this.$vuetify.theme.dark = true
  }
};
</script>
