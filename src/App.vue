<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
import Header from "./components/Header.vue";
import Products from "./components/Products.vue";
import Description from "./components/Description.vue";
import Footer from "./components/Footer.vue";
import Impressum from "./components/Impressum.vue";
import Carousel from "./components/Carousel.vue";
import LoadingSpinner from "./components/util/LoadingSpinner.vue";

import { ref } from "vue";

const currPage = ref("landing");
const childrenLoaded = ref(false);
</script>

<template>
  <div class="kk-content">
    <header>
      <Navigation></Navigation>
      <Header @page-trans="(page) => (currPage = page)" />
    </header>

    <main v-show="childrenLoaded">
      <!--    <Landing v-if="currPage == 'landing'"></Landing> -->

      <Products v-if="currPage == 'landing'"></Products>
      <!--  <Description></Description> -->
      <Carousel
        @imgloaded="(value) => (childrenLoaded = value)"
        v-if="currPage == 'landing'"
      ></Carousel>
      <div v-if="currPage == 'landing'" style="">
        <p>Die Website befindet sich noch im Aufbau.</p>
        <p>In Kürze finden Sie hier weitere Infos!</p>
      </div>
      <Impressum
        @backtolanding="currPage = 'landing'"
        v-if="currPage == 'impressum'"
      ></Impressum>
      <Footer @page-trans="(page) => (currPage = page)"></Footer>
    </main>
    <div v-show="!childrenLoaded" class="kk-loading-spinner">
      <LoadingSpinner></LoadingSpinner>
    </div>
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

.kk-loading-spinner {
  width: 100%;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
