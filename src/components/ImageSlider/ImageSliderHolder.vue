<template>
    <div class="image-slider">
        <h2>Image Slider</h2>
        <p>This carousel can be found at: <a href="https://matthiashager.com/image-slider-vuejs-tutorial">https://matthiashager.com/image-slider-vuejs-tutorial</a></p>
        <ImageSliderCarousel>
             <p>
                <a @click="prev" href='#'>Previous</a> || 
                <a @click="next" href='#'>Next</a>
            </p>
    
            <transition-group name='fade' tag='div'>
            <div v-for="number in [currentNumber]"
                :key='number'>
                <img :src="currentImage"
                     v-on:mouseover="stopRotation"
                     v-on:mouseout="startRotation"/>
            </div>
        </transition-group>
        </ImageSliderCarousel>
    </div>
</template>

<script>
import ImageSliderCarousel from './ImageSliderCarousel';
import ImageSliderSlide from './ImageSliderSlide'

export default {
    name: 'ImageSliderHolder',
    components: {
        ImageSliderCarousel,
        ImageSliderSlide
    },
    data(){
        return {
            images: ['http://i.imgur.com/vYdoAKu.jpg', 'http://i.imgur.com/PUD9HQL.jpg', 'http://i.imgur.com/Lfv18Sb.jpg', 'http://i.imgur.com/tmVJtna.jpg', 'http://i.imgur.com/ZfFAkWZ.jpg'],
            currentNumber: 0,
            timer: null
        };
    },
    computed:{
        currentImage(){
            return this.images[Math.abs(this.currentNumber) % this.images.length];
        }
    },
    methods: {
        next(){
            this.currentNumber += 1;
        },
        prev(){
            this.currentNumber -= 1;
        }
    },

}
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: all 0.8s ease;
  overflow: hidden;
  visibility: visible;
  opacity: 1;
  position: absolute;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
  visibility: hidden;
}
</style>
