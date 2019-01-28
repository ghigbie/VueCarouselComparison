<template>
    <div class='carousel-view'>
    <transition-group
      class='carousel'
      tag="div">
      <div
        v-for="slide in slides" 
        class='slide'
        :key="slide.id">
        <ScratchSlide :title="slide.title"
                      :img="slide.img"
                      :altText="slide.altText"
                      :caption="slide.description"
                      :description="slide.description"/>
      </div>
    </transition-group>
    <div class='carousel-controls'>
      <button class='carousel-controls__button' @click="previous">prev</button>
      <button class='carousel-controls__button' @click="next">next</button>
    </div>
  </div>
</template>


<script>
import ScratchSlide from './ScratchSlide';

export default {
  name: 'CarouselScratch',
  components: {
      ScratchSlide
  },  
  data () {
    return {
      slides: [
        {
          title: 'I am Slide A',
          img: 'http://placekitten.com/g/200/300',
          altText: 'Image of a kitten',
          description: 'Stuff stuff stuff',
          id: 1
        },
        {
          title: 'I am Slide B',
          img: 'http://placekitten.com/g/200/300',
          altText: 'Image of a kitten',
          description: 'Stuff stuff stuff',
          id: 2
        },
        {
          title: 'I am Slide C',
          img: 'http://placekitten.com/g/200/300',
          altText: 'Image of a kitten',
          description: 'Stuff stuff stuff',
          id: 3
        },
        {
          title: 'I am Slide D',
          img: 'http://placekitten.com/g/200/300',
          altText: 'Image of a kitten',
          description: 'Stuff stuff stuff',
          id: 4
        },
        {
          title: 'I am Slide E',
          img: 'http://placekitten.com/g/200/300',
          altText: 'Image of a kitten',
          description: 'Stuff stuff stuff',
          id: 5
        }
      ]
    }
  },
  methods: {
    next () {
      const first = this.slides.shift()
      this.slides = this.slides.concat(first)
    },
    previous () {
      const last = this.slides.pop()
      this.slides = [last].concat(this.slides)
    }
  }
}
</script>

<style>
.carousel-view {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.carousel {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  
  width: 24em;
  min-height: 25em;
}
.slide {
  flex: 0 0 20em;

  margin: 1em;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 0.1em dashed #000;
  transition: transform 0.3s ease-in-out;
}
.slide:first-of-type {
  opacity: 0;
}
.slide:last-of-type {
  opacity: 0;
}
</style>