<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
import Logo from "./components/Logo.vue";
import Products from "./components/Products.vue";
import Description from "./components/Description.vue";
import Footer from "./components/Footer.vue";
import Impressum from "./components/Impressum.vue";
import { ref } from "vue";

const currPage = ref("landing");
</script>

<template>
  <div class="kk-content">
    <header>
      <Logo @page-trans="(page) => (currPage = page)" msg="KAPPES" />
      <!--   <Navigation></Navigation> -->
    </header>

    <main>
      <Landing v-if="currPage == 'landing'"></Landing>

      <!--  <Products></Products> -->
      <!--  <Description></Description> -->
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
    justify-content: space-between;
    line-height: 1;
  }
  main {
    flex: 1;
  }
}
</style>
