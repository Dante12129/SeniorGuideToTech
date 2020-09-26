<template>
  <v-bottom-navigation app grow @change="$emit('change', $event)">
    <v-btn value="Financial">
      <span>Financial</span>
      <v-icon>mdi-alpha-f-box</v-icon>
    </v-btn>

    <v-btn value="Social">
      <span>Social</span>
      <v-icon>mdi-alpha-s-box</v-icon>
    </v-btn>

    <v-btn value="Entertainment">
      <span>Entertainment</span>
      <v-icon>mdi-alpha-e-box</v-icon>
    </v-btn>

    <v-btn value="Shopping">
      <span>Shopping</span>
      <v-icon>mdi-alpha-s-box</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
export default {
  name: "MainNavigation"
}
</script>

<style scoped>

</style>
