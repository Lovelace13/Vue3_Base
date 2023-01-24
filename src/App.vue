<template>
  <v-app>
    <v-card>
      <v-tabs
        v-model="tab"
        bg-color=#F7F7F7
        density="compact"
      >
        <v-tab to="/Ke04">Ke04</v-tab>
        <v-tab to="/about">Ke01</v-tab>
        <v-tab to="/">Ke02</v-tab>
        <v-spacer></v-spacer>
        <v-btn variant="tonal">
          <v-icon size="large">mdi-chat-question-outline</v-icon>
        </v-btn>
      </v-tabs>
    </v-card>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",

  data() {
    return {
      tab: null,
    };
  },
});
</script>
