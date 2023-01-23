<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
    <div class="container-fluid">
      <a class="navbar-brand" href="#"><b>РОС-КЛИНИНГ</b></a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav nav d-flex ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="#price">Калькулятор стоимости</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#typesofwork">Виды работ</a>
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
          <li class="nav-item">
            <a class="nav-link active" href="tel:+79213216653" target="_blank"
              ><u><b>8 (921) 321 66-53</b></u></a
            >
          </li>
          <li class="nav-item">
            <a
              class="nav-link active"
              href="mailto:ros-cleaning@yandex.ru"
              target="_blank"
              ><u><b>ros-cleaning@yandex.ru</b></u></a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "HeaderApp",
};
</script>

<style scoped>
.navbar {
  background-color: #fff !important;
}
.nav-link,
.navbar-brand {
  color: #0d6efd !important;
}
</style>
