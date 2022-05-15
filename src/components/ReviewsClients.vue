<template>
  <div id="reviews" class="mt-5">
    <h2 class="text-center">Отзывы</h2>
    <div class="blocks">
         <img class="stars-left" src="../assets/stars.svg" />
      <div class="right-block mt-5">
        <p>Заказал услуги клининга в первый раз. Даже не думал, что выполнят свою работу настолько быстро и качественно. Рекомендую!</p>
<p><i>Дмитрий, Приладожский</i></p>
      </div>
    </div>
    <div class="blocks">
       <div class="left-block">
        <p>Готовились к переезду, и нужно было максимально быстро отмыть квартиру от предыдущих жильцов. РосКлининг не подвел, теперь обращаемся только к ним!</p>
        <p><i>Ирина и Александр, Санкт-Петербург</i></p>
      </div>
      <img class="stars-right" src="../assets/stars.svg" />
    </div>
    <div class="blocks">
         <img class="stars-left" src="../assets/stars.svg" />
      <div class="right-block">
        <p>Нужно было подготовить арендованное помещение для корпоратива. Знакомый посоветовал РосКлининг. Быстро приехали, оформили заказ, за 2 часа выполнили всю работу. Благодарю!</p>
        <p><i>Борис, Зеленогорск</i></p>
      </div>
     
    </div>
  </div>
</template>

<script>
export default {
  name: "ReviewsClients",
};
</script>
<style scoped>
.blocks{
    display: flex;
    justify-content: space-between;
}
.stars-left{
margin-left: 10%
}
.stars-right{
margin-right: 10%
}
.left-block {
  background: #ffffff;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 0px 30px 30px 0px;
  width: 45vw;
  padding: 20px 0px 20px 100px;
  font-size:max(1em, min(1em, calc(100vw * 4 / 75)));
  line-height: 24px;
  border-left-style: none;
  transition: 0.5s ease;
}
.right-block {
  text-align: right;
  background: #ffffff;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 30px 0px 0px 30px;
  width: 45vw;
  padding: 20px 100px 20px 20px;
  font-size:max(1em, min(1em, calc(100vw * 4 / 75)));
  line-height: 24px;
  margin-left: auto;
  border-right-style: none;
  transition: 0.5s ease;
}


@media screen and (max-width: 992px) {
    .left-block{
        width: 90vw;
        padding: 20px;
         margin-top: 5vh;

    }
     .right-block{
        width: 90vw;
        padding: 20px;
        margin-top: 5vh;
    }
    .stars-left{
        display: none;
    }
    .stars-right{
        display: none;
    }
}

</style>
