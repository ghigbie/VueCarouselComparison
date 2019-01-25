<template>
    <div>
        <h2>Owl Carousel</h2>
        <OwlCarousel>
            <OwlSlide :title=title1 />
            <OwlSlide :title=title2 />
            <OwlSlide :title=title3 />
            <OwlSlide :title=title4 />
            <OwlSlide :title=title5 />
            <OwlSlide :title=title6 />
        </OwlCarousel>
    </div>
</template>

<script>
import OwlCarousel from 'vue-owl-carousel';
import OwlSlide from './OwlSlide';

export default {
    name: 'OwlCarouselHolder',
    data(){
        return{
            title1: 'Stuff 1',
            title2: 'Stuff 2',
            title3: 'Stuff 3',
            title4: 'Stuff 4',
            title5: 'Stuff 5',
            title6: 'Stuff 6'
        }
    },
    components: {
        OwlSlide
    },

}
</script>
