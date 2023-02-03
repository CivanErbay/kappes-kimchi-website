<script setup>
import { ref } from "vue";

const isOpen = ref(true);
</script>

<template>
  <nav class="kk-navi">
    <div class="kk-navi--headlines">
      <h1 @click="$emit('pageTrans', 'landing')" class="kk-headline">KAPPES</h1>
      <div class="">
        <h2 class="kk-subheadline">KIM</h2>
        <h2 class="kk-subheadline">CHI</h2>
      </div>
    </div>

    <div class="kk-navi--inner">
      <a class="kk-navi__product">Produkte</a>
      <a class="kk-navi__principles">Prinzipien</a>
      <a class="kk-navi__contact">Kontakt</a>
    </div>
  </nav>
</template>

<style lang="scss">
.kk-navi {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 25px;

  &--inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    display: none;
  }

  .kk-headline {
    font-family: "Revive80Phatt", sans-serif;
    font-size: 16px;
    padding: 30px 20px 30px 0;
    /*  color: #fff;
    background-color: #181818; */

    cursor: pointer;

    @media screen and (min-width: 768px) {
      font-size: 22px;
    }
  }

  .kk-subheadline {
    font-size: 14px;
  }

  &--headlines {
    display: flex;
    align-items: center;
  }

  .kk-navi {
    a {
      margin: 0 10px;
    }
  }
}
</style>
