<template>
  <v-app>
    <nav-bar></nav-bar>
    <router-view></router-view>
  </v-app>
</template>

<script>
import NavBar from '@/views/NavBar'
export default {
  name: 'App',
  data () {
    return {
      title: process.env.VUE_APP_TITLE
    }
  },
  components: {
    NavBar
  }
}
</script>
