<script setup>
import Landing from "./components/Landing.vue";
</script>

<template>
  <header></header>

  <main>
    <Landing></Landing>
    <!-- <ImgCarousel></ImgCarousel> -->
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
  position: absolute;
  z-index: 1;
  width: 100%;
}

@media (min-width: 1024px) {
  header {
    display: flex;
  }
}
</style>
