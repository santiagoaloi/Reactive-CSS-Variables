<template>
  <v-app-bar app>
    <v-app-bar-nav-icon
      aria-label="Toggle Navigation Drawer"
      @click="drawer = !drawer"
    />

    <v-toolbar-title>Use CSS variables in Vue2</v-toolbar-title>
  </v-app-bar>
</template>

<script>
  // Utilities
  import { sync } from 'vuex-pathify'

  export default {
    name: 'DefaultAppBar',
    computed: { drawer: sync('app/drawer') },
  }
</script>
