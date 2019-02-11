<template>
    <div class="carousel-slide">
        <img class="carousel-img"
             :src="img"
             :alt="altText">
        <h3 class="carousel-slide-title">{{title | slideTitleLength }}</h3>
        <div class="description">
            {{description | sldieDescriptionLength }}
        </div>
    </div>
</template>

<script>
export default {
  name: "HomeogrownSlide",
  props: ["title", "img", "altText", "caption", "description"],
  filters: {
    slideTitleLength(title) {
      if (title.length > 15) {
        title = `${title.substring(0, 16)}...`;
      }
      return title;
    },
    sldieDescriptionLength(description) {
      if (description.length > 75) {
        description = `${description.substring(0, 76)}...`;
      }
      return description;
    }
  }
};
</script>

<style scoped>
.carousel-slide{
    margin: auto 12px auto 12px;
    min-height: 460px;
    text-align: center;
}

.carousel-img{
    width: 320px;
    height: 240px;
}

.carousel-slide-title{
    margin: 8px auto 12px auto;
    color: #254353;
    font-size: 20px;
    line-height: 32px;
    letter-spacing: 1.25px;
}

.carousel-slide-description{
    margin: auto;
    color: #254353;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 1px;
}

</style>
