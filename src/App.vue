<template>
  <v-app>
    <component v-bind:is="layout"></component>
  </v-app>
</template>

<script>
import Login from './layouts/Login'
import Default from './layouts/Default'
export default {
  computed: {
    layout () {
      return this.$store.getters.layout
    }
  },
  components: {
    'login-layout': Login,
    'default-layout': Default
    // define as many layouts you want for the application
  }
}
</script>