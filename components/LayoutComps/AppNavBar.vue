<template>
  <v-app-bar color="primary" dark flat dense>
    <v-toolbar-title>DSF Invoice Mailing System</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn class="mx-1" to="/">Home</v-btn>
    <v-btn class="mx-1" to="/dashboard">Dashboard</v-btn>
    <v-btn class="mx-1" @click="logout">Logout</v-btn>
  </v-app-bar>
</template>

<script>
    import axios from 'axios'
    export default {
        methods: {
            async logout() {
                await axios.get(`http://localhost:3030/api/logout`)
                .then((res) => {
                    console.log(res)
                    this.$router.push('/')
                })
            }
        }
    }
</script>

<style scoped>
</style>