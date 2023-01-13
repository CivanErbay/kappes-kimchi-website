<script setup>
import Landing from "./components/Landing.vue";
import Navigation from "./components/Navigation.vue";
import Logo from "./components/Logo.vue";
import Products from "./components/Products.vue";
import Description from "./components/Description.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <div class="content--kappes">
    <header>
      <Logo msg="KAPPES" />
      <!--   <Navigation></Navigation> -->
    </header>

    <main>
      <Landing></Landing>
      <Footer></Footer>
      <!--  <Products></Products> -->
      <!--  <Description></Description> -->
    </main>
  </div>
</template>

<style lang="scss">
.content--kappes {
  max-width: 1280px;
  margin: 0 auto;

  header {
    display: flex;
    justify-content: space-between;
    line-height: 1;
  }
}
</style>
