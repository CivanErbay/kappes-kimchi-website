<script setup></script>

<template>
  <div class="landing">
    <div class="uc-left"><h3>demnächst verfügbar</h3></div>

    <div class="landing__inner-wrapper">
      <h2 class="headline-m">KIM</h2>
      <h2 class="headline-m flipped">CHI</h2>
    </div>
    <div clasS="uc-right"><h3>coming soon</h3></div>

    <!--  <img class="stage-image__img" src="../assets/kimchi21.jpg" alt="kimchi" /> -->
  </div>
</template>

<style lang="scss">
.landing {
  line-height: 1;
  width: 100%;
  margin: 0 auto;
  text-align: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;

  @media screen and (min-width: 768px) {
    border-top: 5px solid;
    border-bottom: 5px solid;
    margin-top: 50px;
    flex-direction: row;
  }

  &__inner-wrapper {
    border-right: 5px white solid;
    border-left: 5px white solid;

    width: fit-content;
    padding: 50px;

    @media screen and (min-width: 768px) {
    }
  }

  .uc-left {
    border-bottom: 5px solid;
  }

  .uc-right {
    border-top: 5px solid;
  }

  .uc-left,
  .uc-right {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    padding: 30px 0;

    @media screen and (min-width: 768px) {
      border-bottom: 0;
      border-top: 0;
    }
  }
}
</style>
