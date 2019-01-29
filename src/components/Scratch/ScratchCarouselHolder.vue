<template>
    <div class="scratch">
        <h2>From Scratch Carousel Holder</h2>
        <p>This can be found here: <a href="https://medium.com/@davidatomhernandez/how-to-a-simple-carousel-with-vue-138715d615d7">https://medium.com/@davidatomhernandez/how-to-a-simple-carousel-with-vue-138715d615d7</a></p>
        <CarouselScratch />
    </div>
</template>

<script>
import CarouselScratch from './CarouselScratch';

export default {
    name: 'ScratchCarouselHolder',
    components: {
        CarouselScratch
    }
}
</script>
