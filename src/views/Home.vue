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
      <b-card no-body class="overflow-hidden">
        <b-row no-gutters>
          <b-col lg="6">
            <b-card-body>
              <b-card-text>
                <h3 class="card-title">
                  <span class="car-title_underlign">Professionnel</span> et
                  fiable
                </h3>
                <p>
                  EN ECO, <strong>spécialiste de l'isolation</strong>, vous propose de faire des
                  économies d'énergie pour contribuer à la sauvegarde de notre
                  planète en diminuant les gaz à effet de serre par la réduction
                  de vos consommation énergétiques.
                </p>
                <p>
                  En fonction de vos besoins et de votre budget, nos conseillers
                  sauront vous guider vers ce qu'il a de mieux pour vous et
                  votre habitation. Chaque maison est unique, <strong>nous travaillons
                  avec 100% de visites techniques.</strong> Notre directeur technique
                  répondra à toutes vos questions lors de sa venue pour une
                  validation de la faisabilité de vos projets.
                </p>
                <p>
                  Implanté sur Langrune sur mer, nous nous déplaçons sur toute
                  la Normandie. Soucieux de conserver une relation de proximité.
                </p>
                <p>
                  <strong>Nous sommes éligible RGE</strong>, ce qui garantit la qualité et la
                  durabilité de nos matériaux et installations. De plus, nous
                  pouvons vous faire bénéficier du <strong>crédit d'impôt et autres
                  subventions.</strong>
                </p>
                <p>
                  <strong>Contactez-nous pour une demande de visite technique gratuite.</strong>
                </p>
              </b-card-text>
            </b-card-body>
          </b-col>
          <b-col lg="6">
            <b-card-img
              src='../assets/images/home_illustration.png'
              alt="Image"
              class="rounded-0"
            ></b-card-img>
          </b-col>
        </b-row>
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
    @media only screen and (max-width: 720px) {
      h1 {
        font-size: 3rem;
      }
    }
  }
  .card_home {
    display: block;
    margin: 200px auto;
    .card{
      border-color: transparent;
    }
    .card-body {
      padding: 0;
    }
    .card-text {
      padding: 1rem 1rem 0 1rem;
    }
    h3 {
      margin-bottom: 25px;
      color: #285b84;
      font-weight: 600;
      letter-spacing: 1px;
      span {
        padding-bottom: 3px;
        border-bottom: 1px solid #285b8467;
      }
    }
    & > p {
      display: block;
      margin-top: 100px;
    }
  }
}
</style>
