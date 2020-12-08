<template>
  <div class="formContact">
    <h1>{{ title }}</h1>
    <form class="contact-form" @submit.prevent="sendEmail">
      <label>Name</label>
      <input type="text" name="user_name" />
      <label>Email</label>
      <input type="email" name="user_email" />
      <label>Message</label>
      <textarea name="message"></textarea>
      <input type="submit" value="Send" />
    </form>
  </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  name: "FormContact",
  props: {
    title: String,
  },
  methods: {
    sendEmail: (e) => {
      emailjs.sendForm('service_d7yzkun', 'template_suls7od', e.target, 'user_DjSPAKIEOISYGSAvrYotn')
        .then((result) => {
            console.log('SUCCESS!', result.status, result.text);
        }, (error) => {
            console.log('FAILED...', error);
        });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
