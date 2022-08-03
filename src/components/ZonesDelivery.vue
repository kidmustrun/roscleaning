<template>
  <div id="zones" class="pt-5">
    <h2 class="text-center"><b>Зоны обслуживания</b></h2>
    
    <div class="px-5 mt-3 text-md-start text-center cities">
        <p>
            <i>
      Мы работаем в Кировском и Всеволожском районах Ленинградской области,
      Невском районе Санкт-Петербурга, а также в таких населенных пунктах как
      Кировск, Всеволожск, Кудрово, СНТ Восход, Приладожский, Санкт-Петербург,
      Отрадное, Мга, Колпино.
            </i>
      
    </p>
        <div class="zones container">
      <iframe
        class="cart"
        src="https://yandex.ru/map-widget/v1/?um=constructor%3A52d560c004f884349591d37bfa4d042c20465744887791dfe76ae0e99c5de33f&amp;source=constructor"
        width="998"
        height="479"
        frameborder="0"
      ></iframe>
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
.cities{
    font-size: 20px;
    text-align: justify !important;
}
</style>
