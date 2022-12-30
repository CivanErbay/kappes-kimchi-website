<script setup>
import { ref } from "vue";

const isOpen = ref(true);
</script>

<template>
  <nav class="navigation">
    <!-- <div class="navigation--headline">
      <p @click="isOpen = !isOpen">Übersicht</p>
    </div> -->
    <!--  <div :class="{ openNav: isOpen }" class="navigation--content"> -->

    <a class="nav__product">Produkte</a>
    <a class="nav__principles">Prinzipien</a>
    <a class="nav__contact">Kontakt</a>
    <!--   </div> -->
  </nav>
</template>

<style lang="scss">
.navigation {
  display: flex;
  justify-content: flex-end;
  gap: 20px;

  p {
    cursor: pointer;
    font-size: 18px;
    font-weight: 200;
  }
}
</style>
