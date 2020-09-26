<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <h1>Senior Guide To Tech</h1>
    </v-app-bar>

    <v-main>
<!--      <h2>{{ text }}</h2>-->
      <component :is="text"></component>
    </v-main>

    <MainNavigation @change="text = $event"></MainNavigation>
  </v-app>
</template>

<script>
import MainNavigation from "@/components/MainNavigation";
import Financial from "@/components/Financial";

export default {
  name: 'App',

  components: {
    MainNavigation,
    Financial
  },

  data: () => ({
    text: 'Financial'
  }),

  created() {
    this.$vuetify.theme.dark = true
  }
};
</script>
