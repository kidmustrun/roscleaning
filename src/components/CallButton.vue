<template>
  <a
    href="#contacts"
    class="call-button"
    :class="{
      disappear:
        this.scroll < this.windowHeight / 2 &&
        this.windowHeight != 1,
      appear: this.scroll >= this.windowHeight / 2,
      'opacity-0': !this.firstScroll,
    }"
  >
    <div href="#contacts" id="textCall" class="call-text">
      Заказать звонок
    </div>
    <div class="call-image">
      <a href="#contacts"> <img id="imageCall" src="../assets/Vector.svg" /></a>
    </div>
  </a>
</template>

<script>
export default {
  name: "CallButton",
  data() {
    return {
      scroll: window.scrollY,
      windowHeight: 1,
      firstScroll: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
    this.firstView = true;
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll() {
      this.scroll = window.top.scrollY;
      this.windowHeight = window.innerHeight;
      if (this.scroll >= this.windowHeight / 2) {
        this.firstScroll = true;
      }
    },
  },
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
  color: #000000;
  text-decoration: none;
  display: block;
}
.call-text {
  background: #ffffff;
  border: 5px solid #0d6efd;
  box-sizing: border-box;
  border-radius: 100px;
  padding: 10px 45px 10px 30px;
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
.appear {
  opacity: 1;
  animation: appear 0.5s linear;
}
.disappear {
  opacity: 0;
  animation: disappear 0.5s linear;
}
@keyframes appear {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@keyframes disappear {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
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
