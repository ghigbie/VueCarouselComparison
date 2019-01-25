<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <VueCarouselHolder />
    <OwlCarouselHolder />
    <VueFluxHolder />
  </div>
</template>

<script>
import VueCarouselHolder from './VueCarousel/VueCarouselHolder';
import OwlCarouselHolder from './OwlCarousel/OwlCarouselHolder';
import VueFluxHolder from './VueFlux/VueFluxHolder';

export default {
  name: 'ABase',
  props: {
        msg: String
  },
  components: {
    VueCarouselHolder,
    OwlCarouselHolder,
    VueFluxHolder
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
