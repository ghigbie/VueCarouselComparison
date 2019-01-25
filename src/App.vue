<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <CarouselTest msg="Welcome to Your Vue.js App for Testing Prebuilt Carousels"/>
  </div>
</template>

<script>
import CarouselTest from './components/CarouselTest.vue'

export default {
  name: 'app',
  components: {
    CarouselTest
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
