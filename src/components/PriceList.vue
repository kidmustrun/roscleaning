<template>
  <div class="container pt-5" id="price">
    <div class="container-fluid ">
      <form id="form">
        <div class="heading">
          <h2 class="text-center"><b>Калькулятор стоимости уборки</b></h2>
        </div>
        <div class="calc-section">
          <label class="checkbox-wrapper title-bold section-title">
            Тип уборки
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
              <span class="rooms-radio-fake mb-3">Поддерживающая <br />уборка</span>
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
              <span class="rooms-radio-fake mb-3">Генеральная <br />уборка</span>
            </label>

            <label class="rooms-label col col-3-sm text-center">
              <input
                class="rooms-radio-real"
                type="radio"
                name="rooms"
                :value="3"
                v-model.number="type"
              />
              <span class="rooms-radio-fake mb-3">Уборка <br />после ремонта</span>
            </label>
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
              max="750"
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
            max="750"
            step="1"
            v-model.number="room_area"
          />
        </div>
        <div class="calc-section">
          <label
            class="checkbox-wrapper title-bold section-title .section-title--vertical-center"
          >
            <span class="title__inline">Степень загрязнения:</span>
            <input
              type="number"
              min="1"
              max="3"
              id="square-input"
              class="title__inline input-short"
              v-model.number="degree"
            />
         
          </label>
          <input
            type="range"
            id="square-range"
            class="range-input"
            min="1"
            max="3"
            step="1"
            v-model.number="degree"
          />
          <div class="d-flex justify-content-between">
<span>низкая</span>
            <span>средняя</span>
            <span>высокая</span>
          </div>
             
        </div>
        <div class="calc-section">
          <label
            class="checkbox-wrapper title-bold section-title .section-title--vertical-center"
          >
            <span class="title__inline">Количество двустворчатых окон:</span>
            <input
              type="number"
              min="0"
              max="75"
              id="square-input"
              class="title__inline input-short"
              v-model.number="windows"
            />
          </label>
          <input
            type="range"
            id="square-range"
            class="range-input"
            min="0"
            max="75"
            step="1"
            v-model.number="windows"
          />
        </div>
        <div class="calc-section">
          <label
            class="checkbox-wrapper title-bold section-title .section-title--vertical-center"
          >
            <span class="title__inline">Химчистка ковров:</span>
            <input
              type="number"
              min="0"
              max="100"
              id="square-input"
              class="title__inline input-short"
              v-model.number="carpets"
            />
            <span class="title__inline">м²</span>
          </label>
          <input
            type="range"
            id="square-range"
            class="range-input"
            min="0"
            max="100"
            step="1"
            v-model.number="carpets"
          />
        </div>
        <div class="calc-section">
          <label class="checkbox-wrapper title-bold section-title">
            Дополнительные опции
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
              Мойка люстры
              <span class="note">250 рублей</span>
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
              Мойка вытяжки
              <span class="note">450 рублей</span>
            </div>
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
              <span class="note">350 рублей</span>
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
              Мойка духовой/СВЧ печи изнутри
              <span class="note">350 рублей</span>
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
              <span class="note">350 рублей</span>
            </div>
          </label>
        </div>
        <div class="calc-price text-end">
          <h4 class="text-end"><b>Стоимость уборки:</b></h4>
          <div class="calc-price-value">
            <span v-if="total<1000" id="total-price">{{ total }}</span>
             <span v-else id="total-price">{{ (total - total % 1000) / 1000 }} {{ (total%1000).toString().padStart(3,0) }}</span>
            рублей
          </div>
        </div>
      </form>
    </div>
        <h2 class="text-center mt-5"><b>Наши цены</b></h2>
    <div class="container pricelist p-4 mt-4">
      <ul class="list-group list-group-flush">
        <li class="list-group-item d-flex justify-content-between">
          <span>Генеральная уборка</span> <span>от 150 руб/м<sup>2</sup></span>
        </li>
        <li class="list-group-item d-flex justify-content-between">
          <span>Уборка после ремонта</span>
          <span>от 150 руб/м<sup>2</sup></span>
        </li>
        <li class="list-group-item d-flex justify-content-between">
          <span>Поддерживающая уборка</span>
          <span>от 50 руб/м<sup>2</sup></span>
        </li>
        <li class="list-group-item d-flex justify-content-between">
          <span>Мойка окон</span> <span>от 600 руб/м<sup>2</sup></span>
        </li>
        <li class="list-group-item d-flex justify-content-between">
          <span>Химчистка ковров/мягкой мебели</span>
          <span>от 150 руб/м<sup>2</sup></span>
        </li>
        <li class="list-group-item d-flex justify-content-between">
          <span>Дополнительные услуги</span> <span>от 350 руб</span>
        </li>
      </ul>
      <p class="mt-5">
        Точная стоимость зависит от площади помещения и степени загрязнения.
      </p>
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
      degree: 1,
      windows: 0,
      carpets: 0,
      checkedServices: [],
    };
  },
  computed: {
    total: function () {
      let coef = 0;
      switch (this.degree) {
        case 1:
          if (this.type == 2 || this.type == 3) {
            coef = 150;
          } else coef = 50;
          break;
        case 2:
          if (this.type == 2 || this.type == 3) {
            coef = 180;
          } else coef = 70;
          break;
        case 3:
          if (this.type == 2 || this.type == 3) {
            coef = 220;
          } else coef = 90;
          break;
        default:
          if (this.type == 2 || this.type == 3) {
            coef = 150;
          } else coef = 50;
      }
      let summ = 0;
      for (let service of this.checkedServices) {
        if (service == 1) summ += 250;
        else if (service == 2) summ += 450;
        else if (service == 3) summ += 350;
        else if (service == 4) summ += 350;
        else if (service == 5) summ += 350;
      }
      return (
        coef * this.room_area + this.windows * 600 + this.carpets * 150 + summ
      );
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
  padding: 30px 50px;
  /* border: 10px solid #7ac5ea; */
  background-color: rgb(218, 243, 255);
  background-color: white;
  box-shadow: -10px 0px 25px rgba(143, 179, 195, 0.685);
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
