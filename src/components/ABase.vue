<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
    <h2>Vue Carousel</h2>
    <VueCarousel :data="[slide1, slide2, slide3]"/>
    <h2>Owl Carousel</h2>
    <OwlCarousel>
      <OwlSlide :title=title1 />
      <OwlSlide :title=title2 />
      <OwlSlide :title=title3 />
      <OwlSlide :title=title4 />
      <OwlSlide :title=title5 />
      <OwlSlide :title=title6 />
    </OwlCarousel>
    <h2></h2>
  </div>
</template>

<script>
import VueCarousel from '@chenfengyuan/vue-carousel';
import OwlCarousel from 'vue-owl-carousel';
import OwlSlide from './OwlSlide';

export default {
  name: 'ABase',
  components: {
    VueCarousel,
    OwlCarousel,
    OwlSlide
  },
  props: {
    msg: String
  },
  data(){
    return {
      slide1: `<h3>Slide 1</h3>`,
      slide2: `<h3>Slide 2</h3>`,
      slide3: `<h3>Slide 3</h3>`,
      title1:  "Owl Slide 1",
      title2:  "Owl Slide 2",
      title3:  "Owl Slide 3",
      title4:  "Owl Slide 4",
      title5:  "Owl Slide 5",
      title6:  "Owl Slide 6",
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
