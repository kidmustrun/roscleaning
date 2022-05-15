<template>
<div class="hero d-flex progressive replace">
<span class="slogan"><b>РосКлининг<br>Насладитесь<br>чистотой в своем доме</b></span>
</div>
</template>

<script>
export default {
  name: "HeroMain"
}
</script>
<style scoped>
.hero{
    background: url("~@/assets/hero.png") no-repeat center 20%;
    background-size: cover;
    height: 100vh;
    color: white;
    min-height: 340px;
}
.hero.replace {
  background-image: url("~@/assets/hero_small.jpg");
}
.slogan{
    font-size:max(1.5em, min(3.5em, calc(100vw * 4 / 75)));
    white-space: nowrap;
    margin: 20vh 5vw;
}
</style>
