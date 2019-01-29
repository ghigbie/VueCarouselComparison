<template>
    <div class="hooper-carousel-holder">
        <h2>Hooper Carousel</h2>
        <p><a href="https://vuejsexamples.com/a-customizable-carousel-slider-optimized-for-vue/">https://vuejsexamples.com/a-customizable-carousel-slider-optimized-for-vue/</a></p>
        <Hooper>
            <Slide>
                <h3>Yo mamma is so stupid...</h3>
                <p> she thought a pineapple was an apple made out of pine."</p>
            </Slide>
            <Slide>
                <h3>Yo mamma is so small...</h3>
                <p> she tried to hang glide on a dorito."</p>
            </Slide>
            <Slide>
                <h3>Yo mamma is so ugly...</h3>
                <p>she thought Jaba the Hut was pretty."</p>
            </Slide>
            <Navigation slot="hooper-addons"></Navigation>
        </Hooper>
    </div>
</template>

<script>
import { Hooper, Slide, Navigation } from 'hooper';

export default {
    name: 'HooperCarouselHolder',
    components: {
        Hooper,
        Slide,
        Navigation
    }
}
</script>


<style scoped>
.hooper-carousel-holder{

}
</style>
