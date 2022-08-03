<template>
<div class="hero progressive replace">
<h1 class="name"><b>РОС-КЛИНИНГ</b></h1><h2 class="slogan"><b><br>Клининговая компания<br>в Санкт-Петербурге и <br> Ленинградской области</b></h2>
</div>
</template>

<script>
export default {
  name: "HeroMain"
}
</script>
<style scoped>
.hero{
    background: url("~@/assets/hero.jpg") no-repeat;
background-position: center left 20%;
    background-size: cover;
    height: 100vh;
    color: #000;
    min-height: 340px;
}
.hero.replace {
  background-image: url("~@/assets/hero_small.jpg");
}
.name{
    font-size:max(1.5em, min(3.0em, calc(100vw * 4 / 75)));
    /* white-space: nowrap; */
    margin: 30vh 5vw 0 5vw;
     color: #0d6efd !important;
}
.slogan{
    font-size:max(1.5em, min(2.5em, calc(100vw * 4 / 75)));
    /* white-space: nowrap; */
    margin: 0 5vw 0 5vw;
    color: #000000a7 !important;
}
@media screen and (max-width: 576px) {
  .hero{
     background: url("~@/assets/hero_mobile.jpg") no-repeat;
     background-position: center center;
     background-size: cover;
  }
  .name{
    display: none;
  }
  .slogan{
    margin: 30vh 5vw 0 5vw;
}
  .hero.replace {
  background-image: url("~@/assets/hero_mobile_small.jpg");
}
}
</style>
