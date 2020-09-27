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
        <p>ATMs</p>
        <v-container v-if="atms.length !== 0" class="d-md-flex flex-wrap justify-space-around align-center">
            <ATM v-for="(atm, index) in atms" :key="index" :machine="atm"/>
        </v-container>
        <p v-else>No ATMs Found</p>
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
import ATM from "@/components/ATM";

export default {
  name: "Financial",
  components: {
    ATM
  },
  data: function () {
    return {
      pos: null,
      atms: []
    }
  },
  mounted: function () {
    navigator.geolocation.getCurrentPosition(position => {
      console.log(position);
      this.pos = position;
      fetch(`http://api.reimaginebanking.com/atms?lat=${this.pos.coords.latitude}&lng=${this.pos.coords.longitude}&rad=10&key=d9597ddde1565ed544f717ca3004121d`).then(response => response.json()).then(
          data => {
            data.data.forEach(element => this.atms.push(element));
          }
      );
    });
  }
}
</script>

<style scoped>

</style>
