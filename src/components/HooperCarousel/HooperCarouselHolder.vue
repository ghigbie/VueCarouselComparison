<template>
    <div class="hooper-carousel-holder">
        <h2>Hooper Carousel</h2>
        <p><a href="https://vuejsexamples.com/a-customizable-carousel-slider-optimized-for-vue/">https://vuejsexamples.com/a-customizable-carousel-slider-optimized-for-vue/</a></p>

          <hooper :rtl="true">
    <slide>
      slide 1
    </slide>
    <slide>
      slide 2
    </slide>
    ...
  </hooper>
        <Hooper :itemsToShow="3" :centerMode="true" pagination="no">

            <slide>
                <h2>Yo mamma is so stupid...</h2>
                <p> she thought a pineapple was an apple made out of a type of wood."</p>
            </slide>

            <slide>
                <h3>Yo mamma is so small...</h3>
                <p> she tried to hang glide on a dorito."</p>
            </slide>
            <slide>
                <h3>Yo mamma is so ugly...</h3>
                <p>she thought Jaba the Hut was pretty."</p>
            </slide>
            <Navigation slot="hooper-addons"></Navigation>
        </Hooper>

          <hooper>
    <slide>
      slide 1
    </slide>
    <slide>
      slide 2
    </slide>
    ...
  </hooper>
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
