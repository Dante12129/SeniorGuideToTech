<template>
  <v-bottom-navigation v-model="selected" @change="$emit('update:selected', selected)" app grow>
    <v-btn v-for="(cat, index) in categories" :key="index" :value="cat">
      <span>{{ cat }}</span>
      <v-icon>mdi-alpha-{{ cat.charAt(0).toLowerCase() }}-box</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
export default {
  name: "MainNavigation",
  data: function () {
    return {
      selected: '',
      categories: ['Financial', 'Social', 'Entertainment', 'Shopping']
    }
  },
}
</script>

<style scoped>

</style>
