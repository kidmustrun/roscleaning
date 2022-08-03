<template>
  <div class="call-button">
    <div id="textCall" class="call-text">
      <a href="#contacts">Заказать звонок</a>
    </div>
    <div class="call-image">
        <a href="#contacts"> <img id="imageCall" src="../assets/Vector.svg" /></a>
     
    </div>
  </div>
</template>

<script>
export default {
  name: "CallButton"
};
</script>
<style scoped>
.call-button {
    z-index: 100;
  position: fixed;
  bottom: 5vh;
  right: 5vw;
  display: flex;
  flex-direction: row;
}
.call-text {
  background: #ffffff;
  border: 5px solid #0d6efd;
  box-sizing: border-box;
  border-radius: 100px;
  padding: 10px 45px 10px 30px;
}
.call-text a {
  color: #000000;
  text-decoration: none;
}
.call-image {
  background: #0d6efd;
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
