<template>
<div>
  <HeaderApp/>
  <HeroMain/>
  <CallButton/>
  <AboutUs/>
  <TypesOfWork/>
  <ReviewsClients/>
  </div>
</template>

<script>
import HeaderApp from '../components/HeaderApp.vue'
import HeroMain from '../components/HeroMain.vue'
import CallButton from '../components/CallButton.vue'
import AboutUs from '../components/AboutUs.vue'
import TypesOfWork from '../components/TypesOfWork.vue'
import ReviewsClients from '../components/ReviewsClients.vue'

export default {
  name: 'MainPage',
  components: {
    HeaderApp,
    HeroMain,
    CallButton,
    AboutUs,
    TypesOfWork,
    ReviewsClients
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&display=swap');
#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>