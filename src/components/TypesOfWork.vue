<template>
<div class="pt-5" id="typesofwork">
    <h2 class="text-center"><b>Виды работ</b></h2>
    <div class="row mt-4">
        <div class="col col-left mt-md-0 mt-3">
            <div class="text-left text-top">
                Уборка квартир, домов,<br> коммерческих помещений
            </div>
           <img src="../assets/work1.jpg" /> 
        </div>
        <div class="col col-right mt-md-0 mt-3">
            <div class="text-right text-top">
               Удаление<br> Трудновыводимых пятен
            </div>
           <img  src="../assets/work4.jpg" /> 
        </div>
    </div>
    <div class="row">
        <div class="col col-left mt-md-0 mt-3">
            <div class="text-left text-bottom">
                Мойка окон
            </div>
           <img src="../assets/work3.jpg" /> 
        </div>
         <div class="col col-right mt-md-0 mt-3">
            <div class="text-right text-top">
               Химчистка ковров и мягкой мебели
            </div>
           <img  src="../assets/work2.jpg" /> 
        </div>

    </div>
       <div class="row">
           <div class="col col-left mt-md-0 mt-3">
            <div class="text-left text-top">
               Вынос мусора
            </div>
           <img  src="../assets/work6.jpg" /> 
        </div>
        <div class="col col-right mt-md-0 mt-3">
            <div class="text-right text-bottom">
               Дополнительные услуги
          
            </div>
           <img src="../assets/work5.jpg" /> 
        </div>
        
    </div>
  </div>
</template>

<script>
export default {
  name: "TypesOfWork",
};
</script>
<style scoped>
.row{
    margin: 0;
}
img{
    object-fit: cover;
        width: 100vw;
        height: 100%;
        height: 40vh;
    }
.col-right{
    text-align: right;
    padding: 0;
    position: relative;
}
.col-right img{
     border-radius: 30px 0px 0px 30px;
}
.col-left img{
     border-radius: 0px 30px 30px 0px;
}
.col-left{
    padding: 0;
    position: relative;
}
.text-left{
    position:absolute;
    max-width: 90%;
    background-color: rgba(0,0,0,0.5);
    color: #fff;
    padding: 10px 30px 10px 30px;
    font-size:max(1.0em, min(1.2em, calc(100vw * 4 / 75)));
}
.text-right{
    position:absolute;
    max-width: 90%;
    background-color: rgba(0,0,0,0.5);
    color: #fff;
    right: 0;
    padding: 10px 30px 10px 30px;
    font-size:max(1.0em, min(1.2em, calc(100vw * 4 / 75)));
}
.text-top{
 top: 50px;
}
.text-bottom{
    bottom: 50px;
}

@media screen and (min-width: 768px) {
    img{
        width: 90%;
        
    }
    .row{
    margin-top: 5vh;
    }
}
@media screen and (max-width: 768px) {
   .text-left, .text-right{
    background-color: rgba(0,0,0,0.5);
}
img{
    border-radius: 0 0 0 0 !important;
}
}
</style>
