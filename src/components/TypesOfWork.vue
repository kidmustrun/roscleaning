<template>
<div class="mt-5">
    <h2 class="text-center">Виды работ</h2>
    <div class="row mt-4">
        <div class="col col-left">
            <div class="text-left text-top">
                уборка квартир, домов,<br> коммерческих помещений
            </div>
           <img src="../assets/work1.png" /> 
        </div>
        <div class="col col-right">
            <div class="text-right text-bottom">
               химчистка мебели
            </div>
           <img  src="../assets/work2.png" /> 
        </div>
    </div>
    <div class="row">
        <div class="col col-left">
            <div class="text-left text-bottom">
                мойка окон, посуды, <br> крупной бытовой техники
            </div>
           <img src="../assets/work3.png" /> 
        </div>
        <div class="col col-right">
            <div class="text-right text-top">
               удаление<br> трудновыводимых пятен
            </div>
           <img  src="../assets/work4.png" /> 
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
        max-height: 45vh;
    }
.col-right{
    text-align: right;
    padding: 0;
    position: relative;
}

.col-left{
    padding: 0;
    position: relative;
}
.text-left{
    position:absolute;
    background-color: #000;
    color: #fff;
    padding: 10px 70px 10px 30px;
    font-size:max(1.0em, min(1.3em, calc(100vw * 4 / 75)));
}
.text-right{
    position:absolute;
    background-color: #000;
    color: #fff;
    right: 0;
    padding: 10px 30px 10px 70px;
    font-size:max(1.0em, min(1.3em, calc(100vw * 4 / 75)));
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
</style>
