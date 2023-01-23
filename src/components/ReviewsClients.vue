<template>
  <div id="reviews" class="pt-5">
    <h2 class="text-center"><b>Отзывы</b></h2>
    <div
      id="carouselExampleFade"
      class="carousel slide carousel-dark"
      data-bs-ride="carousel"
    >
      <div class="carousel-inner">
        <div class="carousel-item active">
          <div class="blocks">
            <div class="block mt-3 p-3">
              
              <h4 class="text-center"><b>Генеральная уборка дома 200 м²</b></h4>
               <img src="../assets/stars.svg" class="stars"/>
              <p class="mt-3">
                У нас дом 200 кв. м и убрать его своими силами не представляется
                возможным. Потому решили заказать генеральную уборку + мойка
                окон. Работы выполняла бригада из 4-х человек. Уборка была
                выполнена хорошо. Полы оттерли, промыли все полки, во всех
                шкафах. На кухне и в туалете ни следа ржавчины, кухонный
                гарнитур блестит! Средства и пылесосы клинеры принесли свои.
                Спасибо, будем заказывать еще!
              </p>
              <p><i>Ольга и Константин, г. Кировск</i></p>
             
            </div>
          </div>
        </div>
        <div class="carousel-item">
          <div class="blocks">
            <div class="block mt-3 p-3">
               <h4 class="text-center"><b>Химчистка дивана</b></h4>
               <img src="../assets/stars.svg" class="stars"/>
              <p class="mt-3">
                Наш дачный диван уже давно нужно было либо выбросить, либо
                профессионально прохимчистить. Решили дать ему второй шанс и
                обратились в клининговую компанию. На диване было множество
                старых пятен от напитков, просто грязь от времени. Клинер очень
                качественно провёл чистку, вывел неприятные запахи. Всего,
                химчистка заняла 4 часа. Диван стал как новый. Рекомендую!
              </p>
              <p><i>Мария, г. Всеволожск</i></p>
            </div>
          </div>
        </div>
        <div class="carousel-item">
          <div class="blocks">
            <div class="block mt-3 p-3">
              <h4 class="text-center"><b>Уборка после ремонта</b></h4>
               <img src="../assets/stars.svg" class="stars"/>
              <p class="mt-3">
                После ремонта, попробовав убраться самим, быстро поняли, что
                своими силами никак не справимся. Обратились по рекомендации в
                Рос-клининг. Очень понравился подход, все вежливые, аккуратные,
                ребята знают как выводить строительные загрязнения, средства и
                оборудование привезли всё своё. Все было выполнено аккуратно ,
                добросовестно. Работой очень довольна
              </p>
              <p><i>Анастасия, г. Санкт-Петербург</i></p>
            </div>
          </div>
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#carouselExampleFade"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Предыдущий</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#carouselExampleFade"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Следующий</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ReviewsClients",
};
</script>
<style scoped>
.blocks {
  display: flex;
  justify-content: space-between;
}
.stars{
  width: 400px;
}
.block {
  background: #ffffff;
  border: 0.1px solid #000000;
  box-sizing: border-box;
  border-radius: 30px;
  text-align: center;
  margin: 0 auto;
  width: 75%;
  font-size: 1em;
  line-height: 24px;
  transition: 0.5s ease;
}

@media screen and (max-width: 767px) {
  .block{
    font-size: 0.8em;
  }
  .stars{
    width: 100%;
  }
}
</style>
