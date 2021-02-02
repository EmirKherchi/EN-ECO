<template>
  <div class="home">
    <div>
      <b-jumbotron
        class="xyz-in"
        xyz="fade-100% duration-5 ease-in-out"
        :style="{
          backgroundImage:
            'url(' + require('../assets/images/home_jumbotron.png') + ')',
        }"
        header="EN ECO NORMANDIE ISOLATION"
        lead="Société Délégatrice des CEE à 1 Euro"
      >
        <b-button
          class="xyz-in"
          xyz="fade-100% duration-15 ease-in-out delay-3 down-5"
          variant="primary"
          to="/contact"
          >Demandez votre devis</b-button
        >
      </b-jumbotron>
    </div>
    <b-container class="card_home">
      <b-card img-src="https://placekitten.com/300/300" img-alt="Card image" img-right>
      <b-card-text>
        Some quick example text to build on the card and make up the bulk of the card's content.
      </b-card-text>
    </b-card>
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
import "@animxyz/core";
export default {
  name: "Home",
};
</script>

<style lang="scss" scoped>
.home {
  margin-top: 50px;
  .jumbotron {
    border-radius: 0;
    text-align: center;
    color: #fbfbfd;
    background-size: cover;
    height: 600px;
    overflow: hidden;
    h1 {
      margin-top: 80px;
      font-weight: 900;
      letter-spacing: 1px;
    }
    .lead {
      font-weight: 100;
      opacity: 0.7;
      letter-spacing: 1px;
      margin-bottom: 50px;
    }
    .btn-primary {
      color: #fff;
      background-color: #5ea669;
      border: 1px solid #5ea669;

      &:hover {
        background-color: transparent;
        border-color: #fff;
        transition: all 600ms ease;
      }
    }
    @media only screen and (max-width: 600px) {
      h1 {
        font-size: 3rem;
      }
    }
  }
  .card_home{
    
    display: block;
    margin: 200px auto ;
  }
}
</style>
