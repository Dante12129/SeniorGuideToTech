<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <h1>Senior Guide To Tech</h1>
    </v-app-bar>

    <v-main>
      <h2>{{ text }}</h2>
    </v-main>

    <MainNavigation></MainNavigation>
  </v-app>
</template>

<script>
import MainNavigation from "@/components/MainNavigation";
export default {
  name: 'App',

  components: {
    MainNavigation
  },

  data: () => ({
    text: 'Nothing selected yet'
  }),

  created() {
    this.$vuetify.theme.dark = true
  }
};
</script>
