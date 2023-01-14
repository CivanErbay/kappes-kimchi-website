<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
import Logo from "./components/Logo.vue";
import Products from "./components/Products.vue";
import Description from "./components/Description.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <div class="kk-content">
    <header>
      <Logo msg="KAPPES" />
      <!--   <Navigation></Navigation> -->
    </header>

    <main>
      <Landing></Landing>

      <!--  <Products></Products> -->
      <!--  <Description></Description> -->
    </main>

    <Footer></Footer>
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
