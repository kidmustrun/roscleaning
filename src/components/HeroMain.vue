<template>
<div class="hero d-flex">
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
    height: calc(100vh - 56px);
    color: white;
    min-height: 340px;
}
.slogan{
    font-size:max(1.5em, min(3.5em, calc(100vw * 4 / 75)));
    white-space: nowrap;
    margin: 20vh 5vw;
}
</style>
