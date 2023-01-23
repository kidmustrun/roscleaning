<template>
<footer class="footer mt-5" >
  <div class="nav">
<ul class="d-flex justify-content-md-center flex-column flex-md-row mt-3 w-100">
  <li class="nav-item">
          <a class="nav-link" href="#typesofwork">Виды работ</a>
        </li>
         <li class="nav-item">
          <a class="nav-link" href="#price">Калькулятор стоимости</a>
        </li>
         <li class="nav-item">
          <a class="nav-link" href="#zones">Зоны обслуживания</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#reviews">Отзывы</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#contacts">Контакты</a>
        </li>
</ul>

</div>
<p class="cities py-3 px-3 text-md-left text-center">Наши адреса:<br>
Санкт-Петербург, Московский проспект, 74<br>
Ленинградская область, Всеволожск, Октябрьский проспект, 83<br>
Ленинградская область, Кировск, Пионерская улица, 2<br>
Санкт-Петербург, Ленинский проспект, 101Ж</p>
<p class="cities py-3 px-3 mb-3 text-md-left text-center">Кировский район:
Кировск,
Шлиссельбург,
Отрадное,
Мга,
Павлово,
Приладожский,
Синявино,
Назия,
Шум;
Всеволожский район:
Всеволожск,
Кудрово,
Разметелево,
Романовка,
Колпино,
Дубровка,
Островки,
пос. им. Свердлова,
Морозовка,
д. Старая,
Новосаратовка;
Санкт-Петербург:
Невский район,
Дыбенко,
Большевиков,
Ладожская,
Новочеркасская,
Ломоносовская,
Купчино,
Звёздная,
Московская,
Парк победы
</p>
<p class="copyright text-center pb-3">© РОС-КЛИНИНГ. Все права защищены. </p>
</footer>
</template>

<script>
export default {
  name: 'FooterApp'
}
</script>

<style scoped>
.footer{

    background-color: #000;
    box-sizing: border-box;
}
.copyright{
    color: #fff;
}
a{
   color: #ccc
}
li{
    list-style: none;
}
a:hover{
  color: #fff
}

ul{
    margin: 0;
}
  p{
    margin: 0;
  }
  .cities{
    color: #aaa;
    font-size: 1em;
  }
@media screen and (max-width: 576px) {
  .nav ul{
text-align: center;
margin: 0 auto;
padding: 0;
  }
  .nav{
    text-align: center;
    width: 100vw !important;
  }

  
}
</style>
