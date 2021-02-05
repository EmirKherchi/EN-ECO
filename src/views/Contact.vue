<template>
  <div class="contact">
    <b-container>
     <h1>Contactez-nous</h1>
    </b-container>
    
      <FormContact/>
    
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

<style lang="scss" scoped>
 h1 {
   text-align: center;
      margin: 80px auto;
      font-weight: 900;
      letter-spacing: 1px;
      color: #285A84;
    }  
</style>