<template>
  <v-app>
    <router-link to="/users">UsersCard</router-link>
    <router-view />
  </v-app>
</template>

<script>
export default {
  name: 'App'
}
</script>
