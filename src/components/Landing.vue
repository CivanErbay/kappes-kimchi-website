<script setup></script>

<template>
  <div class="landing">
    <div class="landing__inner-wrapper">
      <h2 class="headline-m">KIM</h2>
      <h2 class="headline-m flipped">CHI</h2>
    </div>

    <!--  <img class="stage-image__img" src="../assets/kimchi21.jpg" alt="kimchi" /> -->
  </div>
</template>

<style lang="scss">
.landing {
  line-height: 1;
  width: 100%;
  margin: 0 auto;
  text-align: center;
  border-top: 5px solid;
  /*   padding-top: 50px; */
  margin-top: 50px;
  display: flex;
  justify-content: center;

  &__inner-wrapper {
    border-right: 5px white solid;
    border-left: 5px white solid;
    width: fit-content;
    padding: 50px;
  }
}
</style>
