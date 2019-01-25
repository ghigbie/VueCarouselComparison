<template>
    <div class="vue-flux-holder">
        <h2>Vue Flux Carousel</h2>
        <vue-flux :options="fluxOptions"
                  :images="fluxImages"
                  :transitions="fluxTransitions"
                  ref="slider">
            <!-- <flux-pagination slot="pagination"></flux-pagination> -->
        </vue-flux>
    <button @click="$refs.slider.showImage('prev')">PREV</button>
    <button @click="$refs.slider.showImage('next')">NEXT</button>
    </div>
</template>

<script>
import { VueFlux, FluxPagination, Transitions } from 'vue-flux';

export default {
    name: 'VueFluxHolder',
    components: {
        VueFlux,
        FluxPagination
    },
    data(){
        return {
            fluxOptions: {
                autoplay: true
            },
            fluxImages: [
                'https://amp.businessinsider.com/images/549489a1ecad042f60718e6b-750-500.jpg',
                'https://images.pexels.com/photos/20787/pexels-photo.jpg?cs=srgb&dl=adorable-animal-cat-20787.jpg&fm=jpg',
                'https://www.rd.com/wp-content/uploads/2016/04/01-cat-wants-to-tell-you-laptop.jpg',
                'https://img.washingtonpost.com/rf/image_960w/2010-2019/WashingtonPost/2016/05/24/Editorial-Opinion/Images/Exchange_Zoo_Stray_Cats-0ca3c.jpg',
                'https://images.unsplash.com/photo-1519052537078-e6302a4968d4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&w=1000&q=80',
                'https://vignette.wikia.nocookie.net/houseofnight/images/8/8b/Cats.jpg/revision/latest?cb=20130812053537'
            ],
            fluxTransitions: {
                transitionBook: Transitions.transitionBook
            }
        };
   },
}
</script>

<style scoped>
.vue-flux-holder{
    height: 800px;
}
</style>
