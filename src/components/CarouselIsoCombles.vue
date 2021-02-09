<template>
  <b-container fluid class="Carousel-isocomble">
    <b-container>
      <h2><span>Isolation des</span> combles</h2>
    </b-container>
    <b-container>
      <b-carousel
        id="carousel-fade"
        style="text-shadow: 0px 0px 2px #000"
        fade
        indicators
      >
        <b-carousel-slide
          v-for="image in images"
          v-bind:key="image.id"
          v-bind:img-src="image.path"
        ></b-carousel-slide>
      </b-carousel>
      <p>
        L'isolation de vos combles est très importante pour commencer à faire
        des économies d'énergie et garder au maximum la chaleur de votre maison.
        En effet la déperdition thermique peut s'élever à 30 % de perte par le
        toit
      </p>
    </b-container>
    <hr />
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
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.Carousel-isocomble {
  margin: 0 0 200px 0;
  .carousel {
    display: block;
    margin: 100px auto;
    width: 70%;
    @media only screen and (max-width: 720px) {
      width: 90%;
    }
    &-item {
      height: 600px;
      @media only screen and (max-width: 720px) {
        height: 100%;
      }
      img {
        width: 100%;
        height: 100% !important;
        object-fit: cover;
      }
    }
  }
  h2 {
    color: #111;
    letter-spacing: 1px;
    margin: 25px;
    font-weight: 900;
    @media only screen and (max-width: 720px) {
      text-align: center;
    }
    span {
      padding-bottom: 5px;
      border-bottom: 2px solid #285b8467;
      @media only screen and (max-width: 720px) {
        border: none;
      }
    }
  }
  p {
    color: #111;
    font-size: 18px;
    width: 80%;
    margin: auto;
    @media only screen and (max-width: 720px) {
      width: 100%;
    }
  }
  hr {
    margin-top: 5rem;
    margin-bottom: 1rem;
    border: 0;
    border-top: 1px solid #285b8467;
    width: 80%;
    @media only screen and (max-width: 720px) {
      width: 100%;
    }
  }
}
</style>
