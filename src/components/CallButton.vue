<template>
  <div class="call-button">
    <div class="call-text">
      <a href="#">Заказать звонок</a>
    </div>
    <div class="call-image">
      <img src="../assets/Vector.svg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "CallButton",
};
</script>
<style scoped>
.call-button {
  position: fixed;
  bottom: 5vh;
  right: 5vw;
  display: flex;
  flex-direction: row;
}
.call-text {
  background: #ffffff;
  border: 5px solid #000000;
  box-sizing: border-box;
  border-radius: 100px;
  padding: 10px 45px 10px 30px;
}
.call-text a {
  color: #000000;
  text-decoration: none;
}
.call-image {
  background: #000000;
  border: 5px solid #ffffff;
  box-sizing: border-box;
  border-radius: 100%;
  padding: 10px;
  position: absolute;
  right: -25px;
  top: -10%;
}
@media screen and (max-width: 992px) {
  .call-text {
    display: none;
  }
  .call-image {
    position: static;
  }
}
</style>
