<template>
<div>
  <HeaderApp/>
  <HeroMain/>
  <CallButton/>
  </div>
</template>

<script>
import HeaderApp from '../components/HeaderApp.vue'
import HeroMain from '../components/HeroMain.vue'
import CallButton from '../components/CallButton.vue'
export default {
  name: 'MainPage',
  components: {
    HeaderApp,
    HeroMain,
    CallButton
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