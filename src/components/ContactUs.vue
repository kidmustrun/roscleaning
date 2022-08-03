<template>
  <div id="contacts" class="pt-5">
    <h2 class="text-center"><b>Контакты</b></h2>
    <img class="bubbles-right" src="../assets/bubbles.svg" />
    <div class="row w-100 mt-4">
      <div class="col-lg-5 contacts my-lg-auto">
        <p>Телефон: <a class="link" href="tel:+79211891727" target="_blank" ><u>8 (921) 189 17-27</u></a></p>
        <p>Email: <a class="link" href="mailto:contact@ros-cleaning.ru" target="_blank" ><u>contact@ros-cleaning.ru</u></a></p>
        <p>Социальные сети:</p>
        <div class="d-flex">
          <a href="https://t.me/Roscleaning" class="me-3" target="_blank" >
            <img src="../assets/telegram.svg" />
          </a>
          <a href="https://wa.me/+79211891727" target="_blank"  class="me-3">
            <img src="../assets/whatsapp.svg" />
          </a>
          <a href="https://vk.com/roscleaning" target="_blank" >
            <img src="../assets/vk.svg" />
          </a>
        </div>
      </div>
      <div class="col-lg-7 order-lg-first">
        <div class="form clearfix">
          <h3 class="text-center">Свяжитесь с нами</h3>
          <div class="row g-3 align-items-center mt-3">
            <div class="col-4">
              <label for="name" class="col-form-label required">Ваше имя</label>
            </div>
            <div class="col-8">
              <input
                type="text"
                id="name"
                class="form-control"
                required
                v-model="name"
                placeholder="Иван"
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
                placeholder="Ваш телефон"
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
                placeholder="Нужна уборка квартиры на следующее воскресенье"
              ></textarea>
            </div>
          </div>
          <div class="alert alert-warning mt-3" v-if="warning">
           Вы не заполнили обязательные поля!
          </div>
          <button
            type="button"
            class="btn btn-light mt-3 buttonCall"
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
</template>

<script>
export default {
  name: "ContactUs",
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
.form {
  background: #ddedff;
  border: 1px solid #849fff;
  box-sizing: border-box;
  border-radius: 10px;
  padding: 50px;
  width: 80%;
  margin: 0 auto;
}
label {
  font-size: 1rem;
}
label.required:after {
  color: red;
  content: " *";
  position: absolute;
}
.contacts p {
  font-size: max(0.5em, min(1.3em, calc(100vw * 4 / 75)));
}
.bubbles-right {
  position: absolute;
  right: 0;
  z-index: -1;
  height: inherit;
  max-height: 50vh;
}
.buttonCall {
  float: right;
  border: 1px solid #849fff;
  border-radius: 5px;
  box-sizing: border-box;
}
input {
  border: 1px solid #849fff;
  border-radius: 5px;
}
textarea {
  border: 1px solid #849fff;
  border-radius: 5px;
}
.link{
  color: #000;
}
@media screen and (max-width: 576px) {
  .form {
    margin: 0 auto;
    width: 100%;
    padding: 20px;
  }
  .row {
    padding: 0;
    margin: 0;
  }
}
@media screen and (max-width: 992px) {
  .contacts {
    text-align: center;
    margin-bottom: 3vh;
  }
  .contacts .d-flex {
    justify-content: center;
  }
}
</style>
