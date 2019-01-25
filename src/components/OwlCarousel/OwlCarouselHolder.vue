<template>
    <div>
        <h2>Owl Carousel</h2>
        <p>You can render components withtin this carousel</p>
        <div class="owl-container">
            <OwlCarousel> 
                <OwlSlide :title=title1 />
                <OwlSlide :title=title2 />
                <OwlSlide :title=title3 />
                <OwlSlide :title=title4 />
                <OwlSlide :title=title5 />
                <OwlSlide :title=title6 />
                <OwlSlide :title=title7 />
                <OwlSlide :title=title8 />
                <OwlSlide :title=title9 />
                <OwlSlide :title=title10 />
                <OwlSlide :title=title11 />
                <OwlSlide :title=title12 />
            </OwlCarousel>
        </div>
    </div>
</template>

<script>
import OwlCarousel from 'vue-owl-carousel';
import OwlSlide from './OwlSlide';

export default {
    name: 'OwlCarouselHolder',
    components: {
        OwlCarousel,
        OwlSlide
    },
    data(){
        return{
            title1: 'Stuff 1',
            title2: 'Stuff 2',
            title3: 'Stuff 3',
            title4: 'Stuff 4',
            title5: 'Stuff 5',
            title6: 'Stuff 6',
            title7: 'Stuff 7',
            title8: 'Stuff 8',
            title9: 'Stuff 9',
            title10: 'Stuff 10',
            title11: 'Stuff 11',
            title12: 'Stuff 12',
        }
    }

}
</script>

<style scoped>
.owl-container{
    padding: 0 0 0 5%;
}
</style>
