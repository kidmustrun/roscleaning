<template>
  <div class="container pt-5" id="price">
    <div class="container-fluid">
      <form id="form">
        <div class="heading">
          <h2 class="text-center"><b>Калькулятор стоимости уборки</b></h2>
        </div>
        <div class="calc-section">
          <label class="checkbox-wrapper title-bold section-title">
            Тип уборки:
          </label>
          <div class="rooms-wrapper row">
            <label class="rooms-label col col-3-sm text-center">
              <input
                class="rooms-radio-real"
                type="radio"
                name="rooms"
                :value="1"
                v-model.number="type"
              />
              <span class="rooms-radio-fake mb-3"
                >Поддерживающая <br />уборка</span
              >
            </label>

            <label class="rooms-label col col-3-sm text-center">
              <input
                class="rooms-radio-real"
                type="radio"
                name="rooms"
                :value="2"
                checked
                v-model.number="type"
              />
              <span class="rooms-radio-fake mb-3"
                >Генеральная <br />уборка</span
              >
            </label>

            <label class="rooms-label col col-3-sm text-center">
              <input
                class="rooms-radio-real"
                type="radio"
                name="rooms"
                :value="3"
                v-model.number="type"
              />
              <span class="rooms-radio-fake mb-3"
                >Уборка <br />после ремонта</span
              >
            </label>
            <div class="px-md-5" v-if="this.type == 1">
              <ul>
                <li>Сухая и влажная уборка пола;</li>
                <li>Протирка от пыли всех горизонтальных поверхностей;</li>
                <li>Мойка зеркал;</li>
                <li>Простая чистка и мойка кухни и сан. узлов.</li>
              </ul>
              <div class="accordion" id="accordionExample">
                <div class="accordion-item">
                  <h2 class="accordion-header" id="headingOne">
                    <button
                      class="accordion-button collapsed"
                      type="button"
                      data-bs-toggle="collapse"
                      data-bs-target="#collapseOne"
                      aria-expanded="true"
                      aria-controls="collapseOne"
                    >
                      Полный список услуг, входящих в поддерживающую уборку
                    </button>
                  </h2>
                  <div
                    id="collapseOne"
                    class="accordion-collapse collapse"
                    aria-labelledby="headingOne"
                    data-bs-parent="#accordionExample"
                  >
                    <div class="accordion-body text-start">
                      Сухая и влажная уборка полов, протирка дверей, наличников,
                      плинтусов, бытовой техники, радиаторов, мойка зеркал,
                      протирка смесителей и сантехники, протирка плиты, и
                      кухонной техники, вынос мусора и дезинфекция мусорной
                      корзины.
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="px-md-5" v-if="this.type == 2">
              <ul>
                <li>Сухая и влажная уборка полов;</li>
                <li>
                  Протирка стен, горизонтальных поверхностей, мебели и бытовой
                  техники от пыли;
                </li>
                <li>Удаление въевшихся и трудновыводимых загрязнений;</li>
                <li>Чистка от загрязнений кухонной техники снаружи.</li>
              </ul>
              <div class="accordion" id="accordionExample">
                <div class="accordion-item">
                  <h2 class="accordion-header" id="headingOne">
                    <button
                      class="accordion-button collapsed"
                      type="button"
                      data-bs-toggle="collapse"
                      data-bs-target="#collapseOne"
                      aria-expanded="true"
                      aria-controls="collapseOne"
                    >
                      Полный список услуг, входящих в генеральную уборку
                    </button>
                  </h2>
                  <div
                    id="collapseOne"
                    class="accordion-collapse collapse"
                    aria-labelledby="headingOne"
                    data-bs-parent="#accordionExample"
                  >
                    <div class="accordion-body text-start">
                      Сухая и влажная уборка полов, влажная уборка подоконников,
                      радиаторов, мытьё зеркал и стеклянных поверхностей,
                      влажная уборка всех видов корпусной мебели, удаление пыли
                      с бытовой техники, мытьё дверей, наличников, плинтусов,
                      мойка смесителей и сантехники, мытьё душевой кабины и
                      ванной, мытьё кафельной плитки в санузлах от потолка до
                      пола, мытьё стеновой панели кухонного гарнитура, мытьё
                      внешних фасадов, очистка загрязнений кухонной плиты,
                      вытяжки, духовой и микроволновых печей, холодильника
                      снаружи.
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="px-md-5" v-if="this.type == 3">
              <ul>
                <li>
                  Сбор и вынос строительного мусора , плёнки и картона до 10кг;
                </li>
                <li>
                  Удаление строительной пыли с полов, стен, мебели и техники;
                </li>
                <li>
                  Удаление следов затирки, цемента, лака, краски, клея,
                  строительного скотча;
                </li>
                <li>Включает в себя все услуги генеральной уборки.</li>
              </ul>
              <div class="accordion" id="accordionExample">
                <div class="accordion-item">
                  <h2 class="accordion-header" id="headingOne">
                    <button
                      class="accordion-button collapsed"
                      type="button"
                      data-bs-toggle="collapse"
                      data-bs-target="#collapseOne"
                      aria-expanded="true"
                      aria-controls="collapseOne"
                    >
                      Полный список услуг, входящих в уборку после ремонта
                    </button>
                  </h2>
                  <div
                    id="collapseOne"
                    class="accordion-collapse collapse"
                    aria-labelledby="headingOne"
                    data-bs-parent="#accordionExample"
                  >
                    <div class="accordion-body text-start">
                      Сбор и вынос строительного мусора, плёнки и картона до
                      10кг, удаление строительной пыли с пола, стен, мебели и
                      бытовой техники, удаление следов затирки, цемента, лака,
                      краски, клея, строительного скотча, сухая уборка
                      пылесосом, влажная уборка мебели и бытовой техники, мойка
                      дверей, наличников, плинтусов, мойка зеркал и стеклянных
                      поверхностей, мойка смесителей и сантехники, мытьё душевых
                      кабин и ванн, мытьё кафельной плитки в сан. узлах от
                      потолка до пола, очистка кухонных рабочих поверхностей,
                      мытьё стеновой панели кухонного гарнитура, мытьё внешних
                      фасадов, мойка вытяжки, мытьё кухонной плиты,
                      холодильника, микроволновой и духовой печи снаружи.
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="calc-section">
          <label
            class="checkbox-wrapper title-bold section-title .section-title--vertical-center"
          >
            <span class="title__inline">Площадь помещения:</span>
            <input
              type="number"
              min="0"
              id="square-input"
              class="title__inline input-short"
              v-model.number="room_area"
            />
            <span class="title__inline">м²</span>
          </label>
          <input
            type="range"
            id="square-range"
            class="range-input"
            min="0"
            max="200"
            step="1"
            v-model.number="room_area"
          />
          <div class="d-flex justify-content-between">
            <span><b>0</b></span>
            <span><b>200+</b></span>
          </div>
        </div>
        <div class="calc-section">
          <label
            class="checkbox-wrapper title-bold section-title .section-title--vertical-center"
          >
            <span class="title__inline">Количество окон:</span>
            <input
              type="number"
              min="0"
              id="square-input"
              class="title__inline input-short"
              v-model.number="windows"
            />
          </label>
          <input
            type="range"
            id="square-range"
            class="range-input d-md-block d-none"
            min="0"
            max="20"
            step="1"
            v-model.number="windows"
          />
          <div class="d-md-flex justify-content-between d-none">
            <span><b>0</b></span>
            <span><b>20+</b></span>
          </div>
        </div>
        <div class="calc-section">
          <label class="checkbox-wrapper title-bold section-title">
            Химчистка:
          </label>
          <div class="row container">
            <div class="col-md">
              <label class="radio-wrapper">
                <input
                  type="checkbox"
                  class="radio"
                  name="divan4"
                  value="1"
                  v-model.number="checkedDryCleaning"
                />
                <div class="title-lite">
                  Диван 4-х местный (угловой)
                  <span class="note">4500 рублей</span>
                </div>
              </label>
              <label class="radio-wrapper">
                <input
                  type="checkbox"
                  class="radio"
                  name="divan3"
                  value="2"
                  v-model.number="checkedDryCleaning"
                />
                <div class="title-lite">
                  Диван 3-х местный
                  <span class="note">3500 рублей</span>
                </div>
              </label>
              <label class="radio-wrapper">
                <input
                  type="checkbox"
                  class="radio"
                  name="divan3"
                  value="3"
                  v-model.number="checkedDryCleaning"
                />
                <div class="title-lite">
                  Диван 2-х местный
                  <span class="note">2500 рублей</span>
                </div>
              </label>
            </div>
            <div class="col-md">
              <label class="radio-wrapper">
                <input
                  type="checkbox"
                  class="radio"
                  name="armchair"
                  value="4"
                  v-model.number="checkedDryCleaning"
                />
                <div class="title-lite">
                  Кресло
                  <span class="note">1300 рублей</span>
                </div>
              </label>
              <label class="radio-wrapper">
                <input
                  type="checkbox"
                  class="radio"
                  name="chair"
                  value="5"
                  v-model.number="checkedDryCleaning"
                />
                <div class="title-lite">
                  Стул
                  <span class="note">500 рублей</span>
                </div>
              </label>
              <label class="radio-wrapper">
                <input
                  type="checkbox"
                  class="radio"
                  name="mattress"
                  value="6"
                  v-model.number="checkedDryCleaning"
                />
                <div class="title-lite">
                  Матрас
                  <span class="note">1800 рублей</span>
                </div>
              </label>
            </div>
            <div class="col-md mt-md-0 mt-3">
              <label
                class="checkbox-wrapper title-lite section-title .section-title--vertical-center"
              >
                <div class="title__inline">Ковёр:</div>
                <input
                  type="number"
                  min="0"
                  id="square-input"
                  class="title__inline input-short"
                  v-model.number="carpets"
                />
                <div class="title__inline">м²</div>
              </label>
            </div>
          </div>
        </div>
        <div class="calc-section">
          <label class="checkbox-wrapper title-bold section-title">
            Дополнительные опции
          </label>

          <label class="radio-wrapper">
            <input
              type="checkbox"
              class="radio"
              name="fridge"
              value="3"
              v-model.number="checkedServices"
            />
            <div class="title-lite">
              Мойка холодильника изнутри
              <span class="note">от 350 рублей</span>
            </div>
          </label>
          <label class="radio-wrapper">
            <input
              type="checkbox"
              class="radio"
              name="oven"
              value="4"
              v-model.number="checkedServices"
            />
            <div class="title-lite">
              Мойка микроволновой печи изнутри
              <span class="note">от 350 рублей</span>
            </div>
          </label>
          <label class="radio-wrapper">
            <input
              type="checkbox"
              class="radio"
              name="range_hood"
              value="2"
              v-model.number="checkedServices"
            />
            <div class="title-lite">
              Мойка духовой печи изнутри
              <span class="note">от 450 рублей</span>
            </div>
          </label>
          <label class="radio-wrapper">
            <input
              type="checkbox"
              class="radio"
              name="chandelier"
              value="1"
              v-model.number="checkedServices"
            />
            <div class="title-lite">
              Мойка жалюзи
              <span class="note">от 450 рублей</span>
            </div>
          </label>
          <label class="radio-wrapper">
            <input
              type="checkbox"
              class="radio"
              name="dishes"
              value="5"
              v-model.number="checkedServices"
            />
            <div class="title-lite">
              Мойка посуды
              <span class="note">от 350 рублей</span>
            </div>
          </label>
        </div>
        <div class="calc-price text-end p-md-5 p-3">
          <h4 class="text-end"><b>Примерная стоимость уборки:</b></h4>
          <div class="calc-price-value">
            <span v-if="total < 1000" id="total-price">{{ total }}</span>
            <span v-else id="total-price"
              >{{ (total - (total % 1000)) / 1000 }}
              {{ (total % 1000).toString().padStart(3, 0) }}</span
            >
            рублей
          </div>
            <div class="card card-body container-fluid mt-3">
              <div class="form clearfix">
                <div class="row g-3 align-items-center mt-3 text-center">
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
                      placeholder="Иван"
                    />
                  </div>
                </div>
                <div class="row g-3 align-items-center mt-3 text-center">
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
                <ul class="text-start ms-md-5 mt-5">
                  <li v-if="type == 1 && room_area">Поддерживающая уборка</li>
                  <li v-else-if="type == 2 && room_area">Генеральная уборка</li>
                  <li v-else-if="type == 3 && room_area">
                    Уборка после ремонта
                  </li>
                  <li v-if="room_area">
                    Площадь помещения: {{ room_area }} м²
                  </li>
                  <li v-if="windows">Количество окон: {{ windows }}</li>
                  <li
                    v-if="checkedDryCleaning.find((service) => service == '1')"
                  >
                    Химчистка: Диван 4-х местный (угловой)
                  </li>
                  <li
                    v-if="checkedDryCleaning.find((service) => service == '2')"
                  >
                    Химчистка: Диван 3-х местный
                  </li>
                  <li
                    v-if="checkedDryCleaning.find((service) => service == '3')"
                  >
                    Химчистка: Диван 2-х местный
                  </li>
                  <li
                    v-if="checkedDryCleaning.find((service) => service == '4')"
                  >
                    Химчистка: Кресло
                  </li>
                  <li
                    v-if="checkedDryCleaning.find((service) => service == '5')"
                  >
                    Химчистка: Стул
                  </li>
                  <li
                    v-if="checkedDryCleaning.find((service) => service == '6')"
                  >
                    Химчистка: Матрас
                  </li>
                  <li v-if="carpets">Химчистка: Ковёр {{ carpets }} м²</li>
                  <li v-if="checkedServices.find((service) => service == '3')">
                    Мойка холодильника изнутри
                  </li>
                  <li v-if="checkedServices.find((service) => service == '4')">
                    Мойка микроволновой печи изнутри
                  </li>
                  <li v-if="checkedServices.find((service) => service == '2')">
                    Мойка духовой печи изнутри
                  </li>
                  <li v-if="checkedServices.find((service) => service == '1')">
                    Мойка жалюзи
                  </li>
                  <li v-if="checkedServices.find((service) => service == '5')">
                    Мойка посуды
                  </li>
                </ul>
                <div class="alert alert-warning mt-3" v-if="warning">
                  Вы не заполнили обязательные поля!
                </div>
                <button
                  type="button"
                  class="btn btn-primary mt-3 buttonCall"
                  @click="sendMessage"
                >
                  Отправить заявку
                </button>
                <div class="alert alert-info mt-3" v-if="alert">
                  Спасибо за заявку, мы скоро Вам перезвоним!
                </div>
              </div>
            </div>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: "PriceList",
  data() {
    return {
      type: 2,
      room_area: 0,
      windows: 0,
      carpets: 0,
      checkedServices: [],
      checkedDryCleaning: [],
      name: "",
      phone: "",
      warning: false,
      alert: false
    };
  },
  methods: {
    sendMessage() {
      const axios = require("axios").default;
      if (this.name && this.phone) {
        axios.post(
          `https://api.telegram.org/bot5156932135:AAHQncdNI5AWEzJO0ikk4uHpz4Wu-F7vIvQ/sendMessage?chat_id=-786629935&parse_mode=html&text=Имя: ${this.name}, телефон: ${this.phone}, сообщение: ${this.message}`
        );
        this.warning = false;
        this.alert = true;
      } else this.warning = true;
    },
  },
  computed: {
    total: function () {
      let coef = 0;
      switch (this.type) {
        case 1:
          coef = 60;
          break;
        case 2:
          coef = 150;
          break;
        case 3:
         coef = 170;
          break;
        default:
          coef = 60;
      }
      let summ = 0;
      for (let service of this.checkedServices) {
        if (service == 1) summ += 450;
        else if (service == 2) summ += 450;
        else if (service == 3) summ += 350;
        else if (service == 4) summ += 350;
        else if (service == 5) summ += 350;
      }
      for (let service of this.checkedDryCleaning) {
        if (service == 1) summ += 4500;
        else if (service == 2) summ += 3500;
        else if (service == 3) summ += 2500;
        else if (service == 4) summ += 1300;
        else if (service == 5) summ += 500;
        else if (service == 6) summ += 1800;
      }
      return (
        coef * this.room_area + this.windows * 600 + this.carpets * 150 + summ
      );
    },
    message: function () {
      let stroke = "";
      if (this.type == 1 && this.room_area) stroke += "Поддерживающая уборка, ";
      else if (this.type == 2 && this.room_area)
        stroke += "Генеральная уборка, ";
      else if (this.type == 3 && this.room_area)
        stroke += "Уборка после ремонта, ";
      if (this.room_area) stroke += `площадь помещения: ${this.room_area} м², `;
      if (this.windows) stroke += `количество окон: ${this.windows}, `;
      if (this.checkedDryCleaning.find((service) => service == "1"))
        stroke += "диван 4-х местный (угловой), ";
      if (this.checkedDryCleaning.find((service) => service == "2"))
        stroke += "диван 3-х местный, ";
      if (this.checkedDryCleaning.find((service) => service == "3"))
        stroke += "диван 2-х местный, ";
      if (this.checkedDryCleaning.find((service) => service == "4"))
        stroke += "кресло, ";
      if (this.checkedDryCleaning.find((service) => service == "5"))
        stroke += "стул, ";
      if (this.checkedDryCleaning.find((service) => service == "6"))
        stroke += "матрас, ";
      if (this.carpets) stroke += `ковёр ${this.carpets} м², `;
      if (this.checkedServices.find((service) => service == "3"))
        stroke += "мойка холодильника изнутри, ";
      if (this.checkedServices.find((service) => service == "4"))
        stroke += "мойка микроволновой печи изнутри, ";
      if (this.checkedServices.find((service) => service == "2"))
        stroke += "мойка духовой печи изнутри, ";
      if (this.checkedServices.find((service) => service == "1"))
        stroke += "мойка жалюзи, ";
      if (this.checkedServices.find((service) => service == "5"))
        stroke += "мойка посуды, ";
      if (this.total) stroke += `примерная стоимость ${this.total} рублей`
      return stroke;
    },
  },
};
</script>
<style scoped>
.pricelist {
  border: 3px #0d6efd solid;
  border-radius: 10px;
}
/* ------------------- General ------------------- */

body {
  font-family: "Roboto", sans-serif;
  color: #161616;
  margin: 0;

  padding-bottom: 140px;
}

img {
  max-width: 100%;
  height: auto;
}

.container {
  max-width: 1170px;
  margin-left: auto;
  margin-right: auto;
  /* background-color: aqua; */
}

/* ------------------- Header ------------------- */

.header-inner {
  padding-top: 60px;
  padding-bottom: 60px;
  background-color: #e3f0f7;
}

.header-inner-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.heading-inner {
  font-size: 22px;
  font-weight: 700;
  letter-spacing: 0.26px;
  line-height: 1;
  margin: 0;
}

.heading-inner span {
  display: inline-block;
  line-height: 1;
  margin: 0;
  margin-bottom: 10px;
  font-size: 32px;
  font-weight: 700;
  letter-spacing: 0.38px;
}

.social-icons {
  display: flex;
}

.social-icon-link {
  text-decoration: none;
  margin-right: 30px;
}

/* Для экранов с шириной от 0 до 1170px */
@media (max-width: 1170px) {
  .social-icon-link {
    margin-right: 15px;
    margin-bottom: 15px;
  }
}

/* ------------------- Footer ------------------- */

.footer {
  padding-top: 5px;
  padding-bottom: 30px;
}

.footer-cta-title {
  font-size: 42px;
  font-weight: 700;
  letter-spacing: 0.5px;
  margin-bottom: 25px;
  display: inline-block;
}

.footer-text {
  margin: 0;
  font-size: 18px;
  font-weight: 400;
  letter-spacing: 0.43px;
}

.footer-text a {
  color: #4298e8;
  text-decoration: underline;
}

.footer-cta-text {
  margin: 0;
  font-size: 36px;
  font-weight: 100;
  letter-spacing: 0.43px;
}

.footer-cta-text a {
  color: #4298e8;
  text-decoration: underline;
}

/* Для экранов с шириной от 0 до 1170px */
@media (max-width: 1170px) {
  .footer-cta-title {
    font-size: 26px;
    margin-bottom: 15px;
  }

  .footer-cta-text {
    font-size: 22px;
  }
}

.footer-inner {
  text-align: center;
  padding-bottom: 80px;
}

.text-center {
  text-align: center;
}

/* Calc */

h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0;
}

/* ------------------- Calc ------------------- */
.calc-wrapper {
  padding-top: 50px;
  padding-bottom: 75px;
  max-width: 800px;
  margin: 0 auto;
}

.heading {
  margin-bottom: 50px;
  text-align: center;
}

.heading-title {
  margin: 0;
  margin-bottom: 15px;
  font-size: 40px;
  font-weight: 700;
  line-height: 1;
  letter-spacing: 0.48px;
  text-align: center;
}

.heading-desc {
}

.calc-section {
  padding: 40px 20px;
  background-color: #f4f8fa;
  border-radius: 10px;
}

.calc-section:nth-child(odd) {
  padding: 40px 20px;
  background-color: #fff;
}

.calc-title-light {
  font-size: 24px;
  font-weight: 300;
  margin-bottom: 15px;
}

.title__inline {
  display: inline-block;
  vertical-align: middle;
}

.title__inline + .title__inline {
  margin-left: 10px;
}

.input-short {
  width: 82px;
}

.radio-wrapper {
  display: flex;
  /* align-items: center; */
}

.radio-wrapper .radio {
  margin-top: 9px;
}

.radio-wrapper:not(:last-child) {
  margin-bottom: 30px;
}

.radio-wrapper .radio {
  margin-right: 15px;
  margin-top: 6px;
}

/* .radio-holder {
	margin-right: 15px;
}

.radio-holder input{
	margin-top: 6px;
} */

/* .radio {
	margin-right: 15px;
} */

.input-wrapper {
  display: flex;
  margin-bottom: 40px;
}

.input-wrapper:last-child {
  margin-bottom: 0;
}

.input-short {
  width: 82px;
  height: 36px;
  border-radius: 4px;
  border: 1px solid #9a9a9a;
  font-size: 24px;
  font-weight: 700;
  color: #039be5;
  text-align: center;
  vertical-align: middle;
}

.input-wrapper .input-short:first-child {
  margin-right: 20px;
}

.input-wrapper .input-short:last-child {
  margin-left: 20px;
}

/* ------------ TYPO ------------ */

.section-title {
  margin-bottom: 20px;
}

.section-title--vertical-center {
  align-items: center;
}

.title-bold {
  font-size: 24px;
  font-weight: 700;
}

.title-lite {
  font-size: 20px;
}

.note {
  display: block;
  font-weight: 300;
  font-style: italic;
  padding-top: 10px;
  font-size: 16px;
  color: #969696;
}

/* ------------ FORMS ------------ */

.checkbox-wrapper {
  display: flex;
  margin-bottom: 20px;
  align-items: flex-end;
}

.checkbox-wrapper .checkbox {
  margin-right: 15px;
}

/* ------------ PRICE ------------ */
.calc-price {
  /* border: 10px solid #7ac5ea; */
  background-color: rgb(218, 243, 255);
  background-color: white;
  box-shadow: 0px 0px 25px rgba(143, 179, 195, 0.685);
}

.calc-price-title {
  font-size: 32px;
  font-weight: 700;
  margin-bottom: 10px;
}

.calc-price-value {
  font-size: 26px;
  font-weight: 300;
}

.hidden {
  display: none;
}

.range-input {
  width: 100%;
}

.rooms-wrapper {
  display: flex;
  flex-direction: start;
  align-items: center;
}

.rooms-label {
}
.rooms-radio-real {
  opacity: 0;
  appearance: none;
  height: 0;
  width: 0;
  margin: 0;
}

.rooms-radio-fake {
  display: inline-block;
  padding: 0 30px;
  width: 100%;
  background-color: #e2e2e2;
  text-align: center;
  font-size: 1.25rem;
  /* font-weight: bold; */
  cursor: pointer;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  border-radius: 10px;
}

.rooms-radio-real:checked + .rooms-radio-fake {
  background-color: #fbd422;
}
</style>
