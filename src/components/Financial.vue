<!-- <template>
    <v-list shaped>
      <v-subheader>REPORTS</v-subheader>
      <v-list-item-group v-model="item" color="primary">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
</template>

<script>
  export default {
    data: () => ({
      item: 1,
      items: [
        { text: 'Capital One', icon: 'mdi-alpha-c-box' },
        { text: 'Bank of America', icon: 'mdi-alpha-b-box' },
      ],
    }),
  }
</script> -->

<template>
  <v-expansion-panels>

    <v-expansion-panel>
      <v-expansion-panel-header>Capital One</v-expansion-panel-header>
      <v-expansion-panel-content>
        [Instructions go here]
      </v-expansion-panel-content>
    </v-expansion-panel>

    <v-expansion-panel>
      <v-expansion-panel-header>Bank of America</v-expansion-panel-header>
      <v-expansion-panel-content>
        [Instructions go here]
      </v-expansion-panel-content>
    </v-expansion-panel>

  </v-expansion-panels>
</template>

<script>
export default {
  name: "Financial"
}
</script>

<style scoped>

</style>