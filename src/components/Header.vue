<script setup></script>

<template>
  <div class="kk-logo">
    <div class="kk-logo--header-wrapper">
      <h3>Traditionell.</h3>
      <h3>Handgemacht.</h3>
      <h3>Probiotisch.</h3>
      <div class="kk-logo--header-wrapper--detail-text">
        Produziert in Köln, ausschließlich lokal produziertes Gemüse, intensiv
        im Geschmack & gut für deinen Darm!
      </div>
    </div>

    <div class="kk-logo--image-wrapper">
      <img
        class="kk-logo--image-wrapper--img-one"
        src="../assets/photos/kimchi_circle.jpg"
      />
      <img
        class="kk-logo--image-wrapper--img-two"
        src="../assets/photos/kimchi_open.jpg"
      />
    </div>
  </div>
</template>

<style scoped lang="scss">
.kk-logo {
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
  height: 230px;
  display: flex;
  justify-content: space-between;
  padding: 25px;

  @media screen and (min-width: 1024px) {
    height: 300px;
  }

  &--header-wrapper {
    flex-basis: 50%;
    display: flex;
    flex-direction: column;

    h3 {
      font-weight: 700;
      font-size: 22px;
      margin: 6px 0;

      @media screen and (min-width: 1024px) {
        margin: 10px 0;
        font-size: 34px;
      }
    }

    &--detail-text {
      margin-top: 20px;
      font-size: 12px;
      line-height: 1.5;
      font-family: "Space Grotesk", sans-serif;
      font-weight: 400;
      letter-spacing: 0.5px;

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
      right: 0;
      border: 3px solid white;
      border-radius: 5px;
      z-index: 1;

      @media screen and (min-width: 1024px) {
        height: 250px;
        right: 200px;
        bottom: -25px;
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
      }
    }
  }
}
</style>
