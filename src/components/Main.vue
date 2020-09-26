<template>
<v-list>
  <v-list-item-group v-model="selected">
    <v-list-item v-for="(cat, index) in categories" :key="index">
      <v-list-item-content>
        <v-list-item-title v-text="cat"></v-list-item-title>
      </v-list-item-content>
    </v-list-item>
  </v-list-item-group>
</v-list>
</template>

<script>
export default {
  name: "Main",
  data: function () {
    return {
      selected: 1,
      categories: ['Financial', 'Social', 'Entertainment', 'Shopping']
    }
  }
}
</script>

<style scoped>

</style>
