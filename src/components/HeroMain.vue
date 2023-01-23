<template>
  <div class="hero progressive replace">
    <h1 class="name"><b>РОС-КЛИНИНГ</b></h1>
    <h2 class="slogan">
      <b
        ><br />Клининговая компания<br />в Санкт-Петербурге и <br />
        Ленинградской области</b
      >
    </h2>
    <div class="hero__contacts d-flex">
      <a
        href="https://wa.me/+79213216653"
        target="_blank"
        class="btn btn-success hero__button px-3 py-2"
        ><span>Написать в WhatsApp</span></a
      >
      <div
        data-bs-toggle="modal"
        data-bs-target="#contactUs"
        class="btn btn-primary hero__button px-3 py-2 ms-md-3 mt-md-0"
      >
        <span>Оставить заявку</span>
      </div>
    </div>
    <div
      class="modal fade"
      id="contactUs"
      tabindex="-1"
      aria-labelledby="contactUsLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <div class="order-lg-first">
              <div class="form clearfix">
                <h3 class="text-center">Форма заявки</h3>
                <div class="row g-3 align-items-center mt-3">
                  <div class="col-4">
                    <label for="name" class="col-form-label required"
                      >Ваше имя</label
                    >
                  </div>
                  <div class="col-8">
                    <input
                      type="text"
                      id="name"
                      class="form-control"
                      required
                      v-model="name"
                      placeholder="Светлана"
                    />
                  </div>
                </div>
                <div class="row g-3 align-items-center mt-3">
                  <div class="col-4">
                    <label for="phone" class="col-form-label required"
                      >Ваш телефон</label
                    >
                  </div>
                  <div class="col-8">
                    <input
                      type="tel"
                      id="phone"
                      class="form-control"
                      required
                      v-model="phone"
                      pattern="7\([0-9]{3}\)[0-9]{3}-[0-9]{2}-[0-9]{2}"
                      placeholder="+7(___)__-__"
                    />
                  </div>
                </div>
                <div class="row g-3 align-items-center mt-3">
                  <div class="col-12">
                    <textarea
                      class="form-control"
                      id="message"
                      rows="5"
                      v-model="message"
                      placeholder="Нужна генеральная уборка квартиры 40 метров кв. + мойка окон"
                    ></textarea>
                  </div>
                </div>
                <div class="alert alert-warning mt-3" v-if="warning">
                  Вы не заполнили обязательные поля!
                </div>
                <button
                  type="button"
                  class="btn btn-primary mt-3 buttonCall"
                  @click="sendMessage()"
                  v-if="!alert"
                >
                  Отправить заявку
                </button>
                <div class="alert alert-info mt-3" v-if="alert">
                  Спасибо за заявку, мы скоро Вам перезвоним!
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroMain",
  data() {
    return {
      name: "",
      phone: "",
      message: "",
      alert: false,
      warning: false
    };
  },
  methods: {
    sendMessage() {
      const axios = require("axios").default;
      if(this.name && this.phone){
      axios.post(
        `https://api.telegram.org/bot5156932135:AAHQncdNI5AWEzJO0ikk4uHpz4Wu-F7vIvQ/sendMessage?chat_id=-786629935&parse_mode=html&text=Имя: ${this.name}, телефон: ${this.phone}, сообщение: ${this.message}`
      );
this.warning = false;
      this.alert = true;
      }
      else this.warning = true
    },
  },
};
</script>
<style scoped>
.hero {
  background: url("~@/assets/hero.webp") no-repeat;
  background-position: center left 20%;
  background-size: cover;
  height: 100vh;
  color: #000;
  min-height: 340px;
}
.hero.replace {
  background-image: url("~@/assets/hero_small.webp");
}
.name {
  font-size: max(1.5em, min(3em, calc(100vw * 4 / 75)));
  /* white-space: nowrap; */
  margin: 30vh 5vw 0 5vw;
  color: #0d6efd !important;
}
.slogan {
  font-size: max(1.5em, min(2.5em, calc(100vw * 4 / 75)));
  /* white-space: nowrap; */
  margin: 0 5vw 0 5vw;
  color: #000000a7 !important;
}

.hero__contacts {
  margin: 5vh 5vw 0 5vw;
}

.hero__button {
  max-width: 50%;

  border-radius: 15px;
  text-align: center;
  animation: pulse 3s linear infinite;
}
.hero__button span {
  font-size: max(1.3em, min(1em, calc(100vw * 4 / 75)));
}
.hero__button:first-child span {
  display: inline-block;
  padding-right: 35px;
  text-align: center;
  vertical-align: middle;
}
.hero__button:first-child span:after {
  background: url(../assets/whatsapp.svg);
  content: " ";
  display: inline-block;
  width: 35px;
  height: 1.5em;
  margin-right: -35px;
  margin-left: 6px;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center center;
  vertical-align: -25%;
  text-align: center;
}
.modal-header {
  border: none;
  padding-bottom: 0;
}
.modal-body {
  padding-top: 0;
}
.buttonCall {
  float: right;
  border-radius: 5px;
  box-sizing: border-box;
}
label {
  font-size: 1rem;
}
label.required:after {
  color: red;
  content: " *";
  position: absolute;
}
@keyframes pulse {
  0% {
    transform: scale(0.98);
  }
  50% {
    transform: scale(1);
  }
  100% {
    transform: scale(0.98);
  }
}
@media screen and (max-width: 768px) {
  .hero__contacts {
    display: flex;
    flex-direction: column;
  }

  .hero__button {
    white-space: nowrap;
    max-width: 100%;
  }
  .hero__button:nth-child(2) {
    margin-top: 3vh !important;
    margin-left: 0 !important;
  }
}
@media screen and (max-width: 576px) {
  .hero {
    background: url("~@/assets/hero_mobile.webp") no-repeat;
    background-position: center center;
    background-size: cover;
  }
  .name {
    display: none;
  }
  .slogan {
    margin: 30vh 5vw 0 5vw;
  }
  .hero.replace {
    background-image: url("~@/assets/hero_mobile_small.webp");
  }
}
</style>
