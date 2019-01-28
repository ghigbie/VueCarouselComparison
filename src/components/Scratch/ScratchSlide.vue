<template>
    <div class="scratch-slide">
        <h3>{{title}}</h3>
        <img :src="img" :alt="altText">
        <p>{{caption}}</p>
        <div class="description">
            {{description + ' Meow!'}}
        </div>
    </div>
</template>

<script>
export default {
    name: 'ScratchSlide',
    props: ['title', 'img', 'altText', 'caption', 'description']
}
</script>

