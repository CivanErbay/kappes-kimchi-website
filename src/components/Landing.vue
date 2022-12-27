<script setup>
import Logo from "./Logo.vue";
</script>

<template>
  <div class="landing">
    <div class="stage-image">
      <Logo msg="kappes" />
      <img class="stage-image__img" src="../assets/kimchi21.jpg" alt="kimchi" />
      <div class="border-box"></div>
    </div>
  </div>
</template>

<style lang="scss">
.landing {
  .stage-image {
    position: relative;

    &__img {
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
