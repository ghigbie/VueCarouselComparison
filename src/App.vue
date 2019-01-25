<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <ABase msg="Welcome to Your Vue.js App for Testing Prebuilt Carousels"/>
  </div>
</template>

<script>
import ABase from './components/ABase.vue'

export default {
  name: 'app',
  components: {
    ABase
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
