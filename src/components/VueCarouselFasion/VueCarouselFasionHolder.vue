<template>
    <div class="vue-carousel-fashion">
        <Carousel>
            <SlideContent />
            <SlideContent />
            <SlideContent />
            <SlideContent />
        </Carousel>
    </div>
</template>

<script>
import Carousel from 'vue-carousel';
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
