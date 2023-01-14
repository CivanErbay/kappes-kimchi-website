<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="logo">
    <!-- <h2>김치</h2> -->

    <!-- <h2>KIMCHI</h2> -->
    <!-- <h1>{{ msg }}</h1> -->
    <h1 class="kappes-headline">KAPPES</h1>
  </div>
</template>

<style scoped lang="scss">
.logo {
  width: 100%;

  .kappes-headline {
    font-family: "Revive80Phatt", sans-serif;
    font-size: 32px;
    padding: 30px;
    //padding-bottom: 50px;
    background-color: #fff;
    color: #181818;
    width: 100%;

    @media screen and (min-width: 768px) {
      font-size: 64px;
    }
  }
}
</style>
