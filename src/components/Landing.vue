<script setup>
import Logo from "./Logo.vue";
</script>

<template>
  <div class="landing">
    <div class="stage-image">
      <Logo msg="kappes" />
      <img src="../assets/kimchi21.jpg" alt="kimchi" />
      <div class="border-box"></div>
    </div>

    <div class="landing--subheadline">
      <div class="landing--subheadline__text">
        <h5>biologisch & regional</h5>
        <h5>traditionell & handgemacht</h5>
        <h5>probiotisch & unpasteurisiert</h5>
      </div>

      <img
        class="landing--subheadline--logo"
        src="../assets/gärtopf-white.png"
        alt="gärtopf"
      />
    </div>
  </div>
</template>

<style lang="scss">
.landing {
  &--subheadline {
    display: flex;
    justify-content: center;
    margin-top: 45px;

    @media (min-width: 1024px) {
      margin-top: 35px;
      justify-content: flex-end;
    }

    &--logo {
      height: 115px;

      @media (min-width: 1024px) {
        height: 230px;
      }
    }

    &__text {
      color: white;
      font-size: 24px;
      margin-right: 32px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      font-weight: 300 !important;

      @media (min-width: 1024px) {
        margin-right: 150px;
        font-size: 42px;
        text-align: right;
      }
    }
  }

  .stage-image {
    position: relative;

    img {
      width: 100%;
      object-fit: cover;
      z-index: 0;
      //filter: grayscale(100%);
      animation-name: contentAnim;
      animation-duration: 1s;
      animation-delay: 2s;
      animation-fill-mode: forwards;
      opacity: 0;

      @media (min-width: 1024px) {
        width: 71%;
      }
    }

    .border-box {
      position: absolute;
      width: 59%;
      height: 223px;
      top: 45px;
      right: 10px;
      border: 5px solid white;
      z-index: 2;
      animation-name: contentAnim;
      animation-duration: 1s;
      animation-delay: 2s;
      animation-fill-mode: forwards;
      opacity: 0;

      @media (min-width: 1024px) {
        width: 72%;
        height: 97%;
        top: 30px;
        right: unset;
        left: 15px;
        z-index: 2;
      }
    }

    @keyframes contentAnim {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
  }
}
</style>
