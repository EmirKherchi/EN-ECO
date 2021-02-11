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
  },
  metaInfo: {
      name: 'En Eco Contact',
      title: 'Contact',
      titleTemplate: '%s | EN ECO En Normandie',
      meta: [
                { name: 'description', content:  "Contactez pour un devis gratiut en eco en enormandie d'isolation à un euro en normandie, en eco en normandie vous propose ses services certifiés RGE pour isoler vos maisons par l'extérieur ou depuis vos sous-sol et combles"},
                { property: 'og:title', content: "En Eco En Normandie - Contactez votre entreprise d'isolation à un euro certifiée RGE en Normandie"},
                { property: 'og:site_name', content: 'En Eco En Normandie'},
                {property: 'og:type', content: 'website'},
                 {property: 'og:image', content: '../assets/images/home_jumbotron.png'},
            ]
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