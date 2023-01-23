<template>
  <div id="zones" class="pt-5">
    <h2 class="text-center"><b>Зоны обслуживания</b></h2>

    <div class="container px-md-5 px-2 mt-3 text-md-start text-center cities">
      <div class="zones d-none d-md-block">
        <iframe
          loading="lazy"
          class="cart"
          src="https://yandex.ru/map-widget/v1/?um=constructor%3A52d560c004f884349591d37bfa4d042c20465744887791dfe76ae0e99c5de33f&amp;source=constructor"
          width="998"
          height="479"
          frameborder="0"
        ></iframe>
      </div>
      <div class="zones d-md-none d-block">
        <div style="position: relative; overflow: hidden">
          <iframe
            loading="lazy"
            src="https://yandex.ru/map-widget/v1/-/CCUVFDhhxC"
            width="560"
            height="400"
            frameborder="1"
            allowfullscreen="true"
            style="position: relative"
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ZonesDelivery",
};
</script>
<style scoped>
.zones {
  text-align: center;
}
.cart {
  width: 100%;
  text-align: center;
}
.cities {
  width: 100%;
  font-size: max(1.2em, min(1em, calc(100vw * 4 / 75)));
  text-align: justify !important;
}
</style>
