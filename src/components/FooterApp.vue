<template>
<footer class="footer mt-5" >
  <div class="nav">
<ul class="d-flex flex-column ps-md-5 mt-3">
        <li class="nav-item" >
          <a href="#weare" class="nav-link">О компании</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#reviews">Отзывы</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#contacts">Контакты</a>
        </li>
</ul>
</div>
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
