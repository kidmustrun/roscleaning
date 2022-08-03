<template>
  <div id="reviews" class="pt-5">
    <h2 class="text-center"><b>Отзывы</b></h2>
    <div class="blocks">
         <img class="stars-left" src="../assets/stars.svg" />
      <div class="right-block mt-5">
        <p>Заказали мойку панорамных окон общей площадью 100 метров. Ребята приехали в день обращения со своим оборудованием и химией. Всё быстро и чётко. Я довольна.</p>
<p><i>Лариса, Санкт-Петербург</i></p>
      </div>
    </div>
    <div class="blocks">
       <div class="left-block">
        <p>Перед майскими праздниками надо было срочно привести дом в порядок к приезду гостей. По совету знакомых обратились в эту компанию. Надо было вымыть полы, 200 метров, и протереть пыль по дому. Очень приятный персонал, мы остались очень довольны. В подарок так же сделали химчистку ковра.</p>
        <p><i>Ирина и Александр, Шлиссельбург</i></p>
      </div>
      <img class="stars-right" src="../assets/stars.svg" />
    </div>
    <div class="blocks">
         <img class="stars-left" src="../assets/stars.svg" />
      <div class="right-block">
        <p>Нужна была регулярная поддерживающая уборка торгового помещения 45м.  По совету знакомых выбрали компанию РОС-КЛИНИНГ. Клинеры приезжают без опозданий. Работу выполняют хорошо. Очень вежливые и пунктуальные</p>
        <p><i>Владимир, Санкт-Петербург</i></p>
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
  padding: 20px 20px 20px 100px;
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
