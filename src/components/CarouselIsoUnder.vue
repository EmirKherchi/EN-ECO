<template>
  <b-container fluid class="Carousel-isounder">
    <b-container>
      <h2><span>Isolation sous</span>-sol</h2>
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
           v-bind:img-alt="image.alt"
        ></b-carousel-slide>
      </b-carousel>
      <p>
        L'isolation du sous sol vous apportera un confort de vie optimal. Une
        bonne isolation va permettre une meilleure répartition de l'air ambiant.
        En hiver, il y a une conservation de la chaleur et de la fraîcheur en
        été.
      </p>
    </b-container>
    <hr />
  </b-container>
</template>

<script>
export default {
  name: "CarouselIsoUnder",
  data: function() {
    return {
      images: [
        { id: 1, path: require("@/assets/images/Iso_Under/001.jpeg"), alt: "Images isolations Sous-sol EN Eco en Normandie, Isolation à 1 euro RGE" },
        { id: 2, path: require("@/assets/images/Iso_Under/002.jpeg"),alt: "Images isolations Sous-sol EN Eco en Normandie, Isolation à 1 euro RGE" }, 
        { id: 3, path: require("@/assets/images/Iso_Under/003.jpeg"),alt: "Images isolations Sous-sol EN Eco en Normandie, Isolation à 1 euro RGE" }, 
        { id: 4, path: require("@/assets/images/Iso_Under/004.jpeg"),alt: "Images isolations Sous-sol EN Eco en Normandie, Isolation à 1 euro RGE" },
        { id: 5, path: require("@/assets/images/Iso_Under/005.jpeg"), alt: "Images isolations Sous-sol EN Eco en Normandie, Isolation à 1 euro RGE" }, 
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.Carousel-isounder {
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
    font-weight: 900;
    letter-spacing: 1px;
    margin: 25px;
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
