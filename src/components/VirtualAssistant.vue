<template>
  <v-expansion-panels>
    <v-expansion-panel>
      <v-expansion-panel-header
        >( Dummy) Virtual Assistant
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <div style="text-align:center;">
          <iframe
            style="width: 100%;"
            height="1000"
            width="1000"
            src="https://bot.dialogflow.com/7f6da5c1-629c-4a84-bc08-b486da32654b"
          ></iframe>
        </div>
      </v-expansion-panel-content>
    </v-expansion-panel>

    <v-expansion-panel>
      <v-expansion-panel-header>Explanation </v-expansion-panel-header>
      <v-expansion-panel-content>
        <div style="text-align:center;">
          This is simply a proof of concept right now.
        </div>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</template>

<script>
export default {
  name: "Shopping",
};
</script>

<style scoped></style>
