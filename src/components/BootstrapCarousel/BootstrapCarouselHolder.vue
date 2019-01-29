<template>
    <div class="bootstrap-carousel-holder">
        <h2>Bootstrap Carousel</h2>
        <p>Requires bootstrap to function, but it will hold more than just images</p>
        <BootstrapCarousel />
    </div>
</template>

<script>
import BootstrapCarousel from './BootstrapCarousel';

export default {
    name: 'BootstrapCarouselHolder',
    components: {
        BootstrapCarousel
    }
}
</script>


<style scoped>
.bootstrap-carousel-holder{

}
</style>
