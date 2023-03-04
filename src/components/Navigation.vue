<script setup>
import { ref } from "vue";
import { onMounted } from "vue";

const isOpenNav = ref(false);
const isOpenBurger = ref(false);

onMounted(() => {
  window.addEventListener("scroll", setNavi);
});

const setNavi = () => {
  if (window.pageYOffset > 50) {
    isOpenNav.value = true;
  }
};
const setBurger = () => {
  isOpenBurger.value = !isOpenBurger.value;
};
</script>

<template>
  <nav class="kk-navi">
    <div class="kk-navi--headlines">
      <h1
        @click="$emit('pageTrans', 'landing')"
        :class="{ 'kk-navi--headline-open': isOpenNav }"
        class="kk-headline"
      >
        KAPPES
      </h1>
      <!--   <div class="">
        <h2 class="kk-subheadline">CHI</h2>
      </div> -->
    </div>

    <div @click="setBurger()" class="burger-menu">
      <img
        :class="{ 'visible-burger': isOpenNav }"
        :src="
          isOpenBurger
            ? 'src/assets/illus/chili.png'
            : 'src/assets/illus/Chinakohl-white-bold.png'
        "
        alt="Chinakohl"
      />
    </div>

    <div
      :class="{
        'kk-navi--open': isOpenNav,
        'kk-navi--open-mobile': isOpenBurger,
      }"
      class="kk-navi--text"
    >
      <a class="kk-navi__product">Products</a>
      <a class="kk-navi__principles">About</a>
      <a class="kk-navi__contact">Kontakt</a>
    </div>
    <div></div>
  </nav>
</template>

<style lang="scss">
.kk-navi {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 15px;
  position: fixed;
  z-index: 2;
  width: 100%;
  background-color: black;

  @media (min-width: 1024px) {
    max-width: 1280px;
    padding: 30px 25px;
    justify-content: space-between;
  }

  .kk-headline {
    font-family: "Revive80Phatt", sans-serif;
    font-size: 48px;
    padding-top: 50px;
    color: white;
    cursor: pointer;
    transition: all 1s linear;

    @media (min-width: 1024px) {
      padding-top: 0;
      font-size: 92px;
    }
  }

  &--text {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    color: white;
    transition: all 1s linear;
    transform: translateY(-100px) translateX(-180px);

    @media (min-width: 1024px) {
      gap: 20px;
      position: absolute;
      right: 35px;
      opacity: 0;
      transform: translateY(0) translateX(0);
    }
  }

  .burger-menu {
    position: absolute;
    right: 30px;

    img {
      height: 48px;
      transform: rotate(45deg);
      opacity: 0;
      transition: all 1s linear;
    }

    @media (min-width: 1024px) {
      display: none;
    }
  }

  .visible-burger {
    opacity: 1 !important;
  }

  &--open {
    opacity: 1;
  }

  &--open-mobile {
    transform: translateY(70px) translateX(-180px);
    background-color: black;
    padding: 10px;
  }

  &--headline-open {
    font-size: 32px !important;
    padding-top: 0 !important;
  }

  .kk-subheadline {
    font-size: 14px;
    font-family: "Lexend Zetta", sans-serif;

    &:last-child {
      -moz-transform: scale(-1, 1);
      -webkit-transform: scale(-1, 1);
      -o-transform: scale(-1, 1);
      -ms-transform: scale(-1, 1);
      transform: scale(-1, 1);
      letter-spacing: 1px;
    }
  }

  &--headlines {
    display: flex;
    align-items: center;
  }

  .kk-navi {
    a {
      margin: 0 10px;
    }
  }
}
</style>
