<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
import Products from "./components/Products.vue";
import Description from "./components/Description.vue";
</script>

<template>
  <header>
    <Navigation></Navigation>
  </header>

  <main>
    <div class="wide-bg--green"></div>
    <div class="content-wrapper">
      <Landing></Landing>
      <Products></Products>
      <Description></Description>
    </div>
  </main>
</template>

<style lang="scss">
header {
  max-width: 1280px;
  margin: 0 auto;
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

.content-wrapper {
  max-width: 1280px;
  margin: 0 auto;
}

.wide-bg--green {
  width: 100%;
  margin-top: 31px;
  background-color: #9a4922;
  height: 220px;
  position: absolute;
}
</style>
