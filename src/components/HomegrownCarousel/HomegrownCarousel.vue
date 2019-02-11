<template>
    <div class='carousel-view'>
      <div class="carousel-title">{{ carouselTitle }}</div>
      <transition-group class='carousel'
                        tag="div">
        <div v-for="slide in slides"
             class='slide'
             :key="slide.id">
          <HomegrownSlide :title="slide.title"
                          :img="slide.img"
                          :altText="slide.altText"
                          :caption="slide.description" 
                          :description="slide.description"/>
        </div>
      </transition-group>
      <div class="gradient gradient-left"></div>
      <div class="gradient gradient-right"></div>
      <div class="carousel-controls__button previous-left"
           :class="{active_border: isActiveLeft}"
           @click="previous"></div>
      <div class="carousel-controls__button next-right"
           :class="{active_border: isActiveRight}"
           @click="next"></div>
  </div>
</template>

<script>
import HomegrownSlide from "./CarouselHomegrownSlide";
import slides from "./_carouselData";

export default {
  name: "CarouselHomegrown",
  components: {
    HomegrownSlide
  },
  data() {
    return {
      slides: slides,
      isActiveLeft: false,
      isActiveRight: false
    };
  },
  computed: {
    carouselTitle() {
      const title = "bringing the brand to life";
      return title.toUpperCase();
    }
  },
  methods: {
    next() {
      const first = this.slides.shift();
      this.slides = this.slides.concat(first);
    },
    previous() {
      const last = this.slides.pop();
      this.slides = [last].concat(this.slides);
    },
    checkCarouselLength() {
      if (this.slides.length > 2) {
        this.isActiveLeft = true;
        this.isActiveRight = true;
      }
    }
  },
  created() {
    this.checkCarouselLength();
  }
};
</script>

<style scoped>
.carousel-view {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #254353;
}
.carousel-title{
  color: #008acb;
  font-size: 36px;
  letter-spacing: 2.25px;
  line-height: 48px;
  margin-bottom: 36px;
}
.carousel {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 1200px;
  min-height: 25em;
}
.carousel-controls__button{
  border-top: 5px solid #c4bfbc;
  display: inline-block;
  position: absolute;
  top: 252px;
  width: 22px;
  height: 22px;
  cursor: pointer;
}
.previous-left{
  border-left: 5px solid #c4bfbc;
  transform: rotate(-45deg);
  left: 196px; 
  z-index: 5;
}
.next-right{
  border-right: 5px solid #c4bfbc;
  transform: rotate(45deg);
  right: 196px; 
  z-index: 5;
}
.gradient{
  display: inline-block;
  position: absolute;
  z-index: 3;
  width: 675px;
  height: 460px;
}

.gradient-left{
  background-image: linear-gradient(
    to left,
    rgba(246, 246, 246, 0),
    rgba(246, 246, 246, .7) 12%,
    rgba(246, 246, 246, .8) 15%,
    rgba(246, 246, 246, .9) 18%,
    rgba(246, 246, 246, 1) 20%);
  left: -20%;
}

.gradient-right{
  background-image: linear-gradient(
    to right,
    rgba(246, 246, 246, 0),
    rgba(246, 246, 246, .7) 12%,
    rgba(246, 246, 246, .8) 15%,
    rgba(246, 246, 246, .9) 18%,
    rgba(246, 246, 246, 1) 20%);
  right: -20%;
}

.active_border{
  border-color: #0072a7;
}

.slide {
  flex: 0 0 20em;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s ease-in-out;
}

.slide:first-of-type {
  opacity: 0;
}

.slide:last-of-type {
  opacity: 0;
}

</style>
