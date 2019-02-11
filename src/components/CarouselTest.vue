<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <VueCarouselHolder />
    <OwlCarouselHolder />
    <VueFluxHolder />
    <VueCarouselFashionHolder />
    <ScratchCarouselHolder />
    <!-- <ImageSliderHolder /> -->
    <br>
    <br>
    <BootstrapCarouselHolder />
    <br>
    <HooperCarouselHolder />
    <HomegrownCarousel />
  </div>
</template>

<script>
import VueCarouselHolder from './VueCarousel/VueCarouselHolder';
import OwlCarouselHolder from './OwlCarousel/OwlCarouselHolder';
import VueFluxHolder from './VueFlux/VueFluxHolder';
import VueCarouselFashionHolder from './VueCarouselFasion/VueCarouselFasionHolder';
import ScratchCarouselHolder from './Scratch/ScratchCarouselHolder';
//import ImageSliderHolder from './ImageSlider/ImageSliderHolder';
import BootstrapCarouselHolder from './BootstrapCarousel/BootstrapCarouselHolder';
import HooperCarouselHolder from './HooperCarousel/HooperCarouselHolder';
import HomegrownCarousel from './HomegrownCarousel/HomegrownCarousel';


export default {
  name: 'CarouselTest',
  props: {
        msg: String
  },
  components: {
    VueCarouselHolder,
    OwlCarouselHolder,
    VueFluxHolder,
    VueCarouselFashionHolder,
    ScratchCarouselHolder,
    //ImageSliderHolder,
    BootstrapCarouselHolder,
    HooperCarouselHolder,
    HomegrownCarousel
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
