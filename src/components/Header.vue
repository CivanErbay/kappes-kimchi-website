<script setup>
import VueLoadImage from "vue-load-image";
import LoadingSpinner from "./util/LoadingSpinner.vue";
</script>

<template>
  <div class="kk-header">
    <div class="kk-header--header-wrapper">
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
    </vue-load-image>
  </div>
</template>

<style scoped lang="scss">
.kk-header {
  width: 100%;
  color: white;
  background: rgb(24, 24, 24);
  background: linear-gradient(
    90deg,
    rgba(24, 24, 24, 1) 0%,
    rgba(24, 24, 24, 1) 35%,
    rgba(18, 46, 39, 1) 100%
  );
  position: relative;
  height: 250px;
  display: flex;
  justify-content: space-between;
  padding: 25px;
  padding-left: 15px;

  @media screen and (min-width: 1024px) {
    height: 300px;
    border-radius: 5px;
    padding: 25px;
  }

  &--header-wrapper {
    flex-basis: 50%;
    display: flex;
    flex-direction: column;

    h3 {
      font-weight: 700;
      font-size: 18px;
      margin: 6px 0;

      @media screen and (min-width: 1024px) {
        margin: 10px 0;
        font-size: 34px;
      }
    }

    &--detail-text {
      margin-top: 20px;
      font-size: 11px;
      line-height: 1.5;
      font-family: "Space Grotesk", sans-serif;
      font-weight: 400;
      letter-spacing: 0.5px;
      width: 90%;

      @media screen and (min-width: 1024px) {
        font-size: 15px;
      }
    }
  }

  &--image-wrapper {
    flex-basis: 50%;

    &--img-one {
      height: 125px;
      position: absolute;
      bottom: 50px;
      right: 10px;
      border: 3px solid white;
      border-radius: 5px;
      z-index: 1;

      @media screen and (min-width: 1024px) {
        height: 250px;
        right: 200px;
        bottom: -0;
        border-bottom: 0;
        border-bottom-right-radius: 0;
        border-bottom-left-radius: 0;
      }
    }
    &--img-two {
      height: 100px;
      position: absolute;
      bottom: -25px;
      right: -25px;
      border: 3px solid white;
      border-bottom: 0;
      border-right: 0;
      border-radius: 5px;
      border-bottom-right-radius: 0;
      border-bottom-left-radius: 0;
      border-top-right-radius: 0;

      @media screen and (min-width: 1024px) {
        height: 220px;
        right: -25px;
        top: -25px;

        border: 3px solid white;
        border-top: 0;
        border-right: 0;
        border-top-left-radius: 0;
        border-bottom-right-radius: 0;
        border-top-right-radius: 5px;
      }
    }
  }
  .loading-spinner {
    &-one {
      position: absolute;
      bottom: 20px;
      right: 0;

      @media screen and (min-width: 1024px) {
        bottom: 0;
      }

      .spinner {
        height: 100px;

        @media screen and (min-width: 1024px) {
          height: 200px;
          right: 200px;
          bottom: 0;
          position: absolute;
        }
      }
    }
    &-two {
      .spinner {
        height: 100px;

        @media screen and (min-width: 1024px) {
          height: 200px;
          right: -25px;
          top: -25px;
          position: absolute;
        }
      }
    }
  }
}
</style>
