<template>
  <div class="contact">
    <b-container>
     <h1>Contactez-nous</h1>
    </b-container>
    
      <FormContact/>
      <CardContact/>
    
  </div>
</template>

<script>
// @ is an alias to /src
import FormContact from '@/components/FormContact.vue'
import CardContact from '@/components/CardContact.vue'

export default {
  name: 'Home',
  components: {
    FormContact,
    CardContact
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