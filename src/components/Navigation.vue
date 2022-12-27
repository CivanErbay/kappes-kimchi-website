<script setup>
import { ref } from "vue";

const isOpen = ref(true);
</script>

<template>
  <nav class="navigation">
    <!-- <div class="navigation--headline">
      <p @click="isOpen = !isOpen">Übersicht</p>
    </div> -->
    <div :class="{ openNav: isOpen }" class="navigation--content">
      <p>Produkte</p>
      <p>Prinzipien</p>
      <p>Kontakt</p>
    </div>
  </nav>
</template>

<style lang="scss">
.navigation {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  position: absolute;
  color: white;
  top: 10px;
  left: 15px;

  @media (min-width: 1024px) {
    right: 20px;
    top: 30px;
    align-items: flex-end;
    left: auto;
    width: 100%;
  }

  &--headline {
    font-weight: bold;
    font-size: 22px;
    cursor: pointer;

    @media (min-width: 1024px) {
      font-size: 36px;
    }
  }

  &--content {
    display: flex;
    flex-direction: column;
    opacity: 0;
    font-weight: normal;
    transition: all 0.3s ease-out;
    //transition: padding 1s ease-out;
    /*  border: 5px white solid; */
    font-size: 0px;
    cursor: pointer;
    padding: 0;
    background-color: #181818;

    @media (min-width: 1024px) {
      background-color: transparent;
    }
  }

  .openNav {
    opacity: 1;
    padding: 15px;
    font-size: 24px;
    text-align: right;

    @media (min-width: 1024px) {
      padding: 30px;
      font-size: 32px;
    }
  }
}
</style>
