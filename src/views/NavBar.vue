<template>
  <div>
    <v-toolbar>
      <v-toolbar-items>
        <v-btn
          text
            tag="span"
            style="cursor: pointer"
        >
          Show Case
        </v-btn>
      </v-toolbar-items>

      <v-spacer></v-spacer>

      <v-toolbar-items>
        <v-btn text v-for="item in items" :key="item.title" :to="item.link">
          <v-icon left>{{item.icon}}</v-icon>{{item.title}}
        </v-btn>
        <v-spacer></v-spacer>
      </v-toolbar-items>
    </v-toolbar>
  </div>
</template>

<script>
export default {
  computed: {
    items () {
      const menuItems = [
        {
          title: 'Register',
          icon: 'mdi-face',
          link: '/register'
        },
        {
          title: 'Login',
          icon: 'mdi-lock-open',
          link: '/login'
        },
        {
          title: 'Logout',
          icon: 'mdi-lock',
          link: '/'
        }
      ]
      return menuItems
    }
  }
}
</script>
