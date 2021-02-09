<template>
  <b-container class="card_contact">
    <b-card no-body class="overflow-hidden">
      <b-row no-gutters>
        <b-col lg="6">
          <b-card-img
            src="../assets/images/contact_illustration.png"
            alt="Image"
            class="rounded-0"
          ></b-card-img>
        </b-col>
        <b-col lg="6">
          <b-card-body>
            <b-card-text>
              <b-row>
                <b-col lg="6">
                  <b-list-group>
                    <b-list-group-item>
                      <b-icon icon="telephone-fill"></b-icon> 
                      06021144485</b-list-group-item
                    >
                    <b-list-group-item>
                      <b-icon icon="envelope"></b-icon>
                      email@email.fr</b-list-group-item
                    >
                    <b-list-group-item
                      ><b-icon icon="geo-alt-fill"></b-icon> adresse<br />127
                      rue de l'adresse <br />
                      14000 adresse</b-list-group-item
                    >
                  </b-list-group>
                </b-col>
                <b-col lg="6">
                  <b-list-group>
                    <b-list-group-item>Instragram</b-list-group-item>
                    <b-list-group-item>Facebook</b-list-group-item>
                    <b-list-group-item>logo</b-list-group-item>
                  </b-list-group>
                </b-col>
              </b-row>
            </b-card-text>
          </b-card-body>
        </b-col>
      </b-row>
    </b-card>
  </b-container>
</template>

<script>
import "@animxyz/core";

export default {
  name: "CardContact",

  data: function() {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.card_contact {
  margin: 200px auto;
  .list-group-item {
    padding-left: 50px;
    border: none;
    margin-bottom: 20%;
    color: #68717a;
  }
  .card-img {
    width: 90%;
  }
}
</style>
