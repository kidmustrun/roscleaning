<template>
<footer class="footer mt-5" >
<ul class="d-flex flex-column">
        <li class="nav-item" >
          <a href="#weare" class="nav-link">О нас</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#reviews">Отзывы</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#contacts">Контакты</a>
        </li>
</ul>
<p class="copyright text-center mt-2">© РосКлининг. Все права защищены. </p>
</footer>
</template>

<script>
export default {
  name: 'FooterApp'
}
</script>

<style scoped>
.footer{
    height: 170px;
    background-color: #000;
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
</style>
