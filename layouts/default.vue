<template>
  <v-app dark>
    <v-content>
      <app-nav-bar></app-nav-bar>
      <div class="py-6"></div>
      <nuxt></nuxt>
      <div class="py-6"></div>
      <app-foot-bar></app-foot-bar>
    </v-content>
  </v-app>
</template>

<script>
import AppNavBar from '../components/LayoutComps/AppNavBar'
import AppFootBar from '../components/LayoutComps/AppFootBar'
export default {
  components: {
    AppNavBar,
    AppFootBar
  }
}
</script>
