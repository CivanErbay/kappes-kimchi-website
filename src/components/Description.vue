<script setup></script>

<template>
  <div class="description-content">
    <div class="description-content__text">
      <p>biologisch & regional</p>
      <p>traditionell & handgemacht</p>
      <p>probiotisch & unpasteurisiert</p>
    </div>

    <img
      class="description-content--logo"
      src="../assets/gärtopf-logo.png"
      alt="gärtopf"
    />
  </div>
</template>

<style lang="scss">
.description {
  &-content {
    display: flex;
    justify-content: center;
    margin-top: 45px;

    @media (min-width: 1024px) {
      margin-top: 35px;
      justify-content: flex-end;
    }

    &--logo {
      height: 115px;

      @media (min-width: 1024px) {
        height: 230px;
      }
    }

    &__text {
      font-size: 24px;
      margin-right: 32px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      font-weight: 300 !important;

      @media (min-width: 1024px) {
        margin-right: 150px;
        font-size: 42px;
        text-align: right;
      }
    }
  }
}
</style>
