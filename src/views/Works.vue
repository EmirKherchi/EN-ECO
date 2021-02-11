<template>
  <div class="Works">
    <b-container fluid center>
      <h1>Nos Réalisations</h1>
    </b-container>
    <CarouselIsoCombles/>
    <CarouselIsoUnder/>
  </div>
</template>

<script>
// @ is an alias to /src
import CarouselIsoCombles from '@/components/CarouselIsoCombles.vue'
import CarouselIsoUnder from '@/components/CarouselIsoUnder.vue'

export default {
  name: 'Home',
  components: {
    CarouselIsoCombles,
    CarouselIsoUnder
  },
  metaInfo: {
      name: 'En Eco Nos réalisations',
      title: 'Nos réalisations',
      titleTemplate: '%s | EN ECO En Normandie',
      meta: [
                { name: 'description', content:  "Découvrez nos réalisations en eco en enormandie d'isolation à un euro en normandie, en eco en normandie vous propose ses services certifiés RGE pour isoler vos maisons par l'extérieur ou depuis vos sous-sol et combles"},
                { property: 'og:title', content: "En Eco En Normandie - Découvrez nos réalisations d'isolations d'habitations en Normandie"},
                { property: 'og:site_name', content: 'En Eco En Normandie'},
                {property: 'og:type', content: 'website'},    
                {name: 'robots', content: 'index,follow'} 
            ]
    }
}
</script>

<style lang="scss" scoped>
h1 {
    margin: 50px 0 100px 0px;
    text-align: center;
    color: #111;
    font-weight: 900;
    letter-spacing: 1px;
    color: #285b84;
  }
  
</style>