<template>
  <v-app>
    <v-app-bar app dark dense>
      <v-app-bar-title>Yakui</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn to="/" text>
        <span class="mr-2">Main</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
      <v-btn to="/about" text>
        <span class="mr-2">About</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class extends Vue {}
</script>
