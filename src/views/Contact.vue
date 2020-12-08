<template>
  <div class="contact">
    <b-container>
     <h1>contact</h1>
    </b-container>
    <b-container>
      <FormContact/>
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
import FormContact from '@/components/FormContact.vue'

export default {
  name: 'Home',
  components: {
    FormContact
  }
}
</script>