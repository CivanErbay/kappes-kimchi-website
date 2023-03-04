<script setup>
import VueLoadImage from "vue-load-image";
</script>

<template>
  <div class="kk-header">
    <!-- <div class="kk-header--header-wrapper">
      <h3>Traditionell.</h3>
      <h3>Handgemacht.</h3>
      <h3>Probiotisch.</h3>
      <div class="kk-header--header-wrapper--detail-text">
        Produziert in Köln, ausschließlich lokal erzeugtes Gemüse, intensiv im
        Geschmack & gut für deinen Darm!
      </div>
    </div>

    <vue-load-image class="loading-spinner-one">
      <template v-slot:image>
        <img
          id="img-one"
          class="kk-header--image-wrapper--img-one"
          alt="kimchi-glas-circle-lying"
          src="../assets/photos/kimchi_circle.jpg"
        />
      </template>
      <template v-slot:preloader> </template>
      <template v-slot:error>Image load fails</template>
    </vue-load-image>

    <vue-load-image class="loading-spinner-two">
      <template v-slot:image>
        <img
          id="img-two"
          class="kk-header--image-wrapper--img-two"
          alt="kimchi-on-ceramic-floor"
          src="../assets/photos/kimchi_open.jpg"
        />
      </template>
      <template v-slot:preloader> </template>
      <template v-slot:error>Image load fails</template>
    </vue-load-image> -->
    <!--     <div class="kk-header--navi"><h1 class="kk-headline">KAPPES</h1></div> -->

    <!--  <div class="kk-subheadline-wrapper">
      <h2 class="kk-subheadline">KIM</h2>
      <h2 class="kk-subheadline">CHI</h2>
    </div> -->
  </div>
</template>

<style scoped lang="scss">
.kk-header {
  height: 100vh;
  background: url("../assets/photos/kimchi_circle.jpg");
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;

  &--navi {
    .kk-headline {
      font-family: "Revive80Phatt", sans-serif;
      font-size: 92px;
      margin-top: 30px;
      color: white;
    }

    position: fixed;
  }
}
</style>
