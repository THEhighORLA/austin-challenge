<template>
  <div id="app">
      <landing-page></landing-page>
  </div>
</template>

<script>
import LandingPage from './components/LandingPage.vue'

export default {
  name: 'App',
  components: {
    LandingPage
  }
}
</script>

<style>
@import './assets/styles/main';

body {
  background-color: #080c20;
}
</style>
