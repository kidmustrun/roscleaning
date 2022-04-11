<template>
  <div class="mt-5">
    <h1 id="weare" class="text-center">О компании</h1>
    <div class="blocks mt-4">
        <img class="bubbles-left" src="../assets/bubbles_left.svg" />
         <img class="bubbles-right" src="../assets/bubbles.svg" />
        
         
      <div class="left-block mt-5">
        <p>проводим клининговые работы</p>
        <p>работаем в СПБ и ЛО</p>
        <img src="../assets/spb.svg" />
      </div>
      <div class="right-block">
        <p>занимаемся всеми видами услуг</p>
        <p>от уборки до удаления пятен</p>
        <img src="../assets/clean.svg" />
      </div>
      <div class="left-block">
        <p>имеем опыт работы более 5 лет</p>
        <p>сохраняем доступную стоимость</p>
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
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 0px 30px 30px 0px;
  width: 45vw;
  padding: 20px 0px 20px 100px;
  font-size:max(0.5em, min(1.5em, calc(100vw * 4 / 75)));
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
  padding: 20px 100px 20px 0px;
  font-size:max(0.5em, min(1.5em, calc(100vw * 4 / 75)));
  line-height: 24px;
  margin-left: auto;
  border-right-style: none;
  transition: 0.5s ease;
}
.left-block:hover {
  background: #ddedff;
  border: 1px solid #849fff;
  border-left-style: none;
  cursor: pointer;
  box-sizing: border-box;
  transition: 0.5s ease;
}
.right-block:hover {
  background: #ddedff;
  border: 1px solid #849fff;
  border-right-style: none;
  cursor: pointer;
  box-sizing: border-box;
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
@media screen and (max-width: 1200px) {
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
    .left-block img{
        max-width: 70vw;
    }
     .right-block img{
        max-width: 70vw;
    }
}
@media screen and (max-width: 768px) {
    .bubbles-left{
   display: none;
}
}
</style>
