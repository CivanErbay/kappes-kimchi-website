<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
import Header from "./components/Header.vue";
import Products from "./components/Products.vue";
import Description from "./components/Description.vue";
import Footer from "./components/Footer.vue";
import Impressum from "./components/Impressum.vue";
import Carousel from "./components/Carousel.vue";

import { ref } from "vue";

const currPage = ref("landing");
</script>

<template>
  <div class="kk-content">
    <header>
      <Navigation></Navigation>
      <Header @page-trans="(page) => (currPage = page)" />
    </header>

    <main>
      <!--    <Landing v-if="currPage == 'landing'"></Landing> -->

      <!--  <Products></Products> -->
      <!--  <Description></Description> -->
      <Carousel v-if="currPage == 'landing'"></Carousel>
      <div
        v-if="currPage == 'landing'"
        style="
          font-size: 14px;
          margin: 20px 10px;
          font-family: 'Space Grotesk', sans-serif;
        "
      >
        <p>Die Website befindet sich noch im Aufbau.</p>
        <p>In Kürze finden Sie hier weitere Infos!</p>
      </div>
      <Impressum v-if="currPage == 'impressum'"></Impressum>
    </main>

    <Footer @page-trans="(page) => (currPage = page)"></Footer>
  </div>
</template>

<style lang="scss">
.kk-content {
  max-width: 1280px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  margin: 0 auto;

  header {
    display: flex;
    flex-direction: column;
    line-height: 1;
  }
  main {
    flex: 1;
  }
}
</style>
