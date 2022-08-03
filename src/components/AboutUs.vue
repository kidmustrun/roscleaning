<template>
  <div class="pt-5" id="weare">
    <h2  class="text-center"><b>О компании</b></h2>
    <div class="blocks mt-4">
        <img class="bubbles-left" src="../assets/bubbles_left.svg" />
         <img class="bubbles-right" src="../assets/bubbles.svg" />
        
         
      <div class="left-block mt-5">
        <p>Проводим клининговые работы
        в СПБ и ЛО</p>
        <img src="../assets/spb.svg" />
      </div>
      <div class="right-block">
        <p>Предоставляем полный спектр
        <br>клининговых услуг</p>
        <img src="../assets/clean.svg" />
      </div>
      <div class="left-block">
        <p>Имеем двухлетний опыт работы
        <br>Сотрудничаем с малым и средним бизнесом
        <br>Наши клиенты нам доверяют</p>
        <img src="../assets/quality.svg" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutUs",
};
</script>
<style scoped>
.blocks{
    position: relative;
}
.left-block {
  background: #ffffff;
border: 3px solid #849fff;
  box-sizing: border-box;
  border-radius: 0px 30px 30px 0px;
  width: 45vw;
  padding: 20px 0px 20px 100px;
  font-size:max(0.5em, min(1.2em, calc(100vw * 4 / 75)));
  line-height: 24px;
  border-left-style: none;
  transition: 0.5s ease;
}
.right-block {
  text-align: right;
  background: #ffffff;
border: 3px solid #849fff;
  box-sizing: border-box;
  border-radius: 30px 0px 0px 30px;
  width: 45vw;
  padding: 20px 100px 20px 0px;
  font-size:max(0.5em, min(1.2em, calc(100vw * 4 / 75)));
  line-height: 24px;
  margin-left: auto;
  border-right-style: none;
  transition: 0.5s ease;
}
.bubbles-right{
    position: absolute;
    right: 0;
    z-index: -1;
    height: inherit;
    max-height: 100vh;
}
.bubbles-left{
    position: absolute;
    left: 0;
    bottom: 30px;
    z-index: -1;
    height: inherit;
}
.left-block img{
  width: 40%;
}
.right-block img{
  width: 40%;
}
@media screen and (max-width: 1200px) {
    .left-block{
        width: 70vw;
        padding: 20px;
         margin-top: 5vh;
    }
     .right-block{
        width: 70vw;
        padding: 20px;
         margin-top: 5vh;
    }
    .left-block img{
        width: 70%;
        max-width: 30vw;
    }
     .right-block img{
        width: 70%;
        max-width: 30vw;
    }
}
@media screen and (max-width: 768px) {
    .bubbles-left{
   display: none;
}

}
@media screen and (max-width: 576px) {
 .left-block img{
        width: 90%;
        max-width: 80vw;
    }
     .right-block img{
        width: 90%;
        max-width: 80vw;
    }
}
</style>
