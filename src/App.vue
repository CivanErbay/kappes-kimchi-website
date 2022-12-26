<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
</script>

<template>
  <header>
    <Navigation></Navigation>
  </header>

  <main>
    <Landing></Landing>
    <!-- <ImgCarousel></ImgCarousel> -->
  </main>
</template>

<style lang="scss">
header {
  position: relative;
  z-index: 1;
  width: 100%;
  opacity: 0;
  animation-name: headerAppear;
  animation-duration: 1s;
  animation-delay: 2s;
  animation-fill-mode: forwards;

  @media (min-width: 1024px) {
  }

  @keyframes headerAppear {
    0% {
      opacity: 0;
    }
    20% {
    }
    100% {
      opacity: 1;
    }
  }
}
</style>
