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