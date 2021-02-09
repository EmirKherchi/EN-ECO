<template>
  <b-container fluid class="formContact">
    <b-container class="formContact_container-child" v-if="status == ''">
      <b-form inline class="contact-form" @submit.prevent="sendEmail">
        <b-form-row>
          <b-form-group id="input-firstname" label-for="input-firstname">
            <b-form-input
              id="input-firstname"
              type="text"
              name="user_firstname"
              placeholder="Prénom"
              required
          /></b-form-group>

          <b-form-group id="input-name" label-for="input-name">
            <b-form-input
              type="text"
              name="user_name"
              placeholder="Nom"
              required
          /></b-form-group>

          <b-input-group
            id="input-email"
            label="Email:"
            label-for="input-email"
            prepend="@"
          >
            <b-form-input
              type="email"
              name="user_email"
              placeholder="E-mail"
              required
          /></b-input-group>
        </b-form-row>

        <b-form-row>
          <b-form-group id="input-phone" label-for="input-phone">
            <b-form-input
              id="input-phone"
              type="tel"
              name="user_phone"
              placeholder="Téléphone"
              required
          /></b-form-group>

          <b-form-group id="input-city" label-for="input-city">
            <b-form-input
              type="text"
              name="user_city"
              placeholder="Ville"
              required
          /></b-form-group>

          <b-form-group id="input-postCode" label-for="input-postCode">
            <b-form-input
              type="text"
              name="user_postCode"
              placeholder="Code postal"
              required
          /></b-form-group>
        </b-form-row>

        <b-form-row>
          <b-form-col>
            <h6>Travaux à effectuer :</h6>
            <b-form-checkbox
              type="checkbox"
              name="iso_comble"
              id="iso_comble"
              value="Isolation des combles"
              >Isolation des combles</b-form-checkbox
            >

            <b-form-checkbox
              type="checkbox"
              name="iso_sous"
              id="iso_sous"
              value="Isolation du sous sol"
            >
              Isolation du sous-sol</b-form-checkbox
            >
            <b-form-checkbox
              type="checkbox"
              name="iso_vide"
              id="iso_vide"
              value="Isolation vide sanitaire"
            >
              Isolation du sous-sol</b-form-checkbox
            >
            <b-form-checkbox
              type="checkbox"
              name="iso_ext"
              id="iso_ext"
              value="Isolation éxtérieur"
              >Isolation extérieur</b-form-checkbox
            >
          </b-form-col>

          <b-form-col>
            <h6>Message:</h6>
            <b-form-textarea
              name="message"
              placeholder="Description de votre projet ...."
              rows="6"
              max-rows="6"
            >
            </b-form-textarea>
          </b-form-col>
        </b-form-row>

        <b-container>
          <b-button type="submit" value="Send">Envoyer</b-button>
        </b-container>
      </b-form>
    </b-container>
    <h2
      class="xyz-in"
      xyz="fade down-100% back-5 ease-in-out"
      v-if="status === 'ok'"
    >
      Merci votre message est envoyé, nous vous contacterons dans les plus brefs
      délais.
    </h2>
    <h3
      class="xyz-in"
      xyz="fade down-100% back-5 ease-in-out"
      v-if="status === 'nope'"
    >
      Une erreur est survenue, veuillez recommencer
    </h3>
   
  </b-container>
</template>

<script>
import emailjs from "emailjs-com";
import "@animxyz/core";

export default {
  name: "FormContact",
  props: {
    title: String,
  },
  data: function() {
    return {
      status: "",
    };
  },
  methods: {
    sendEmail: function(e) {
      emailjs
        .sendForm(
          "service_d7yzkun",
          "template_suls7od",
          e.target,
          "user_DjSPAKIEOISYGSAvrYotn"
        )
        .then(
          (result) => {
            console.log("SUCCESS!", result.status, result.text);
            this.status = "ok";
            status();
          },
          (error) => {
            console.log("FAILED...", error);
            this.status = "nope";
          }
        );
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.formContact {
  background-color: #fff;
  padding: 50px 0 100px 0px;
  .form-inline {
    display: block;
    margin-left: 15%;
  }
  .form-group {
    margin-right: 50px;
  }
  .form-row {
    margin-bottom: 100px;
    @media only screen and (max-width: 720px) {
      display: block;
      margin: 15px auto;
    }
  }
  .input-group > .custom-file,
  .input-group > .custom-select,
  .input-group > .form-control,
  .input-group > .form-control-plaintext {
    max-width: 189px;
    @media only screen and (max-width: 720px) {
      max-width: 245px;
    }
    @media only screen and (max-width: 375px) {
      max-width: 201px;
    }
  }
  b-form-col {
    margin-right: 150px;
    .custom-control {
      margin-bottom: 15px;
    }
    h6 {
      margin-bottom: 20px;
      font-weight: 600;
      @media only screen and (max-width: 720px) {
        margin-top: 25px;
      }
    }
    textarea {
      @media only screen and (max-width: 720px) {
        max-width: 240px;
      }
      width: 200%;
    }
  }
  button {
    display: block;
    margin-left: 37%;
    text-align: center;
    color: #fff;
    background-color: #5ea669;
    border: 1px solid #5ea669;
    @media only screen and (max-width: 720px) {
      margin-left: 25%;
    }

    &:hover {
      background-color: transparent;
      border-color: #111;
      color: #111;
      transition: all 600ms ease;
    }
  }
  h2,
  h3 {
    text-align: center;
    color: #5ea669;
    padding-top: 50px;
     margin-bottom: 500px;
  }
 
}
</style>
