<script setup></script>

<template>
  <div class="kk-logo">
    <div class="kk-logo--headline-wrapper">
      <h1 @click="$emit('pageTrans', 'landing')" class="kappes-headline">
        KAPPES
      </h1>
      <div class="">
        <h2 class="headline-m">KIM</h2>
        <h2 class="headline-m flipped">CHI</h2>
      </div>
    </div>

    <img class="kk-logo--img-one" src="../assets/photos/kimchi23.jpg" />
  </div>
</template>

<style scoped lang="scss">
.kk-logo {
  width: 100%;
  display: flex;
  justify-content: space-between;

  &--headline-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .kappes-headline {
    font-family: "Revive80Phatt", sans-serif;
    font-size: 32px;
    padding: 30px;
    color: #fff;
    background-color: #181818;
    width: 100%;
    cursor: pointer;

    @media screen and (min-width: 768px) {
      font-size: 64px;
    }
  }

  &--img-one {
    height: 200px;
  }
}
</style>
