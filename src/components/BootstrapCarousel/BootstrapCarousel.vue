<template>
    <div class="container" id="app">
        <div class="row">
            <div class="col-10 mx-auto">
                <template id="carousel-template">
            <div>
                <div id="carouselExample" class="carousel slide" data-ride="carousel" data-interval="6000">
                    <div class="carousel-inner">
                        <div class="carousel-item" 
                             v-for="(banner,index) in banners" 
                             :key="index"
                             :class="{ active: idx==0 }">
                            <p>adfafaf</p>
                            <img :src="banner" alt="" class="img-fluid">
                        </div>
                    </div>
                </div>
            </div>
        </template>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BootstrapCarousel',
    data () {
    return {
      banners:["//placehold.it/1200x600","//placehold.it/1200x600/333/fff","//placehold.it/1200x600/cc2222"]
    }
  }
}
</script>

<style scoped>

</style>

