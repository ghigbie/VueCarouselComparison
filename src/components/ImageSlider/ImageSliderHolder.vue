<template>
    <div class="image-slider">
        <h2>Image Slider</h2>
        <ImageSliderCarousel />
    </div>
</template>

<script>
import ImageSliderCarousel from './ImageSliderCarousel';
import ImageSliderSlide from './ImageSliderSlide'

export default {
    name: 'ImageSldierHolder',
    components: {
        ImageSliderCarousel,
        ImageSliderSlide
    }
}
</script>

<style scoped>
.image-slider{

}
</style>
