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
                      <b-icon icon="telephone-fill"></b-icon><a href="tel:+33642242283">
                     06 42 24 22 83</a></b-list-group-item
                    >
                    <b-list-group-item>
                      <b-icon icon="envelope"></b-icon><a href="mailto:sas.en.eco@gmail.com">
                      sas.en.eco@gmail.com</a></b-list-group-item
                    >
                    <b-list-group-item
                      ><b-icon icon="geo-alt-fill"></b-icon> EN ECO<br />12 Rue de Luc<br />
                      14830 Langrune-sur-Mer</b-list-group-item
                    >
                  </b-list-group>
                </b-col>
                <b-col lg="6">
                  <b-list-group>
                    <b-list-group-item>
                      <router-link tag="li" to="/mentions"
                        ><a
                          ><b-img
                            src="../assets/images/Instagram_logo.png"
                            alt="Instagram entreprise isolation 1euro en eco normandie"
                          /> Instagram</a
                        ></router-link
                      ></b-list-group-item>
                    <b-list-group-item>
                      <router-link tag="li" to="/mentions"
                        ><a
                          ><b-img
                            src="../assets/images/Facebook_logo.png"
                            alt="Facebook entreprise isolation 1euro en eco normandie"
                          /> Facebook</a
                        ></router-link
                      ></b-list-group-item>
                    <b-list-group-item><b-img
                            src="../assets/images/logo.png"
                            alt="Logo entreprise isolation 1euro en eco normandie"
                          /></b-list-group-item>
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

export default {
  name: "CardContact",
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.card_contact {
  li{
    list-style: none;
    
  }
  svg{
    margin-right: 5px;
    margin-left: -25px;
    color: #000;
     @media screen and (max-width: 991px) {
      margin-left: -15px;
      
    }
  }
  a{
    color: #68717a;
    &:hover{
      text-decoration: none;
      color: #5ea669 !important;
      transition: all 300ms ease-out;
    }
  }

  margin: 200px auto;
  .list-group-item {
    padding-left: 50px;
    border: none;
    margin-bottom: 20%;
    color: #68717a;
    @media screen and (max-width: 991px) {
     text-align: center;
      margin-bottom: 5%;
       padding-left: 0px;
    }
  }
  
}
</style>
