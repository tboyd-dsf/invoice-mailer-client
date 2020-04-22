<template>
  <v-row>
    <v-col cols="12" md="6" offset-md="3">
      <v-card class="mx-auto mt-5">
        <v-card-title>
          <h1 class="display-1">Login</h1>
        </v-card-title>
        <v-form>
          <v-card-text>
            <v-text-field label="Username" v-model="email" prepend-icon="mdi-account-circle" />
            <v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Password"
              v-model="password"
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            />
          </v-card-text>
          <v-divider></v-divider>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn @click.prevent="loginUser" type="submit" color="info">Login</v-btn>
          </v-card-actions>
        </v-form>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      showPassword: false,
      email: '',
      password: ''
    }
  },
  methods: {
    async loginUser() {
      alert('Wow you logged in. Nice!')
      await axios.post(`http://localhost:3030/api/login`, {
        email: this.email,
        password: this.password
      })
      .then((res) => {
        console.log(res)
        this.$router.push('/dashboard')
        this.email = ''
        this.password = ''
      })
    }
  }
}
</script>

<style scoped>
</style>