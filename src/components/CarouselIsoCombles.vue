<template>
  <b-container class="Carousel">
    <b-carousel
      id="carousel-fade"
      style="text-shadow: 0px 0px 2px #000"
      fade
      indicators
      img-width="800"
      img-height="480"
    >
      <b-carousel-slide
        v-for="image in images"
        v-bind:key="image.id"
        v-bind:img-src="image.path"
        img-width="800"
        img-height="480"
      ></b-carousel-slide>
    </b-carousel>
  </b-container>
</template>

<script>
export default {
  name: "CarouselIsoCombles",
  data: function() {
    return {
      images: [
        { id: 1, path: require("@/assets/images/Iso_combles/001.jpeg") },
        { id: 2, path: require("@/assets/images/Iso_combles/002.jpeg") },
        { id: 3, path: require("@/assets/images/Iso_combles/003.jpeg") },
        { id: 4, path: require("@/assets/images/Iso_combles/004.jpeg") },
      ],
    };
  },
  props: {
    title: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.Carousel {
  display: block;
  margin: 100px auto;
}
</style>
