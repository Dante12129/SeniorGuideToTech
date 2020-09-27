<template>
  <v-card color="secondary" min-width="350px">
    <v-card-title>{{ machine.name }}</v-card-title>
    <v-card-text>{{ address }}</v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "ATM",
  props: {
    machine: Object
  },
  computed: {
    address: function () {
      let state = this.machine.address.state;
      let zip = this.machine.address.zip;
      let city = this.machine.address.city;
      let street = this.machine.address.street_name;
      let number = this.machine.address.street_number;
      return `${number} ${street} \n${city}, ${state} ${zip}`;
    }
  }
}
</script>

<style scoped>
</style>
