<template>
  <div class="formContact">
    <form class="contact-form" @submit.prevent="sendEmail">
      <label>Name</label>
      <input type="text" name="user_name" />
      <label>Email</label>
      <input type="email" name="user_email" />
      <label for="iso_comble">Isolation des combles</label>
      <input
        type="checkbox"
        name="iso_comble"
        id="iso_comble"
        value="isolation des combles"
      />
      <label for="iso_sous">Isolation du sous-sol</label>
      <input
        type="checkbox"
        name="iso_sous"
        id="iso_sous"
        value="isolation du sous sol"
      />
      <label>Message</label>
      <textarea name="message"></textarea>

      <input type="submit" value="Send" />
      
    </form>
  </div>
</template>

<script>
import emailjs from "emailjs-com";

export default {
  name: "FormContact",
  props: {
    title: String,
  },
  data: function() {
    return {
      isocomble: false,
    };
  },
  methods: {
    sendEmail: (e) => {
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
          },
          (error) => {
            console.log("FAILED...", error);
          }
        );
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.formContact {
  text-align: center;
  input {
    display: block;
    margin: auto;
    &[type="submit"] {
      margin-top: 50px;
    }
  }
  textarea {
    display: block;
    margin: auto;
  }
}
</style>
