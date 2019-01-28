<template>
    <div class="vue-carousel-fashion">
    <h2>Vue Carousel Fashion</h2>
        <Carousel :navigationEnabled="false">
            <SlideContent />
            <SlideContent />
            <SlideContent />
            <SlideContent />
            <SlideContent />
            <SlideContent />
        </Carousel>
    </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
import SlideContent from './SlideContent';

export default {
    name: 'VueCarouselFashionHolder',
    components: {
        Carousel,
        SlideContent
    }
    
}
</script>

<style scoped>
.vue-carousel-fashion{

}
</style>
