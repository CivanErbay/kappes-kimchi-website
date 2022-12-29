<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
import Products from "./components/Products.vue";
import Description from "./components/Description.vue";
</script>

<template>
  <div class="content--kappes">
    <header>
      <Navigation></Navigation>
    </header>

    <main>
      <Landing></Landing>
      <!--  <Products></Products> -->
      <!--  <Description></Description> -->
    </main>
  </div>
</template>

<style lang="scss">
.content--kappes {
  max-width: 1280px;
  margin: 0 auto;
}
</style>
