<template>
    <div class="owl-slide">
        {{title}}
    </div>

</template>


<script>
export default {
    name: 'OwlSlide',
    props: ['title'],
    data(){
        return {

        };
    },

}
</script>


<style scoped>
    .owl-slide{
        color: #000;
        font-weight: 900;
        width: 300px;
        height: 200px;
        background-color: rgb(134, 134, 177);
    }
</style>
