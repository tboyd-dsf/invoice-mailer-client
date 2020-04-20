<template>
  <v-row>
    <v-col cols="12" md="6" offset-md="3">
      <v-card class="mx-auto mt-5">
        <v-card-title>
          <h1 class="display-1">Login</h1>
        </v-card-title>
        <v-form>
          <v-card-text>
            <v-text-field label="Username" prepend-icon="mdi-account-circle" />
            <v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Password"
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            />
          </v-card-text>
          <v-divider></v-divider>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn @click="loginUser" type="submit" color="info">Login</v-btn>
          </v-card-actions>
        </v-form>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      showPassword: false
    }
  },
  methods: {
    loginUser() {
      alert('Wow you logged in. Nice!')
    }
  }
}
</script>

<style scoped>
</style>