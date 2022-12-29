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
    <p>Produkte</p>
    <p>Prinzipien</p>
    <p>Kontakt</p>
    <!--   </div> -->
  </nav>
</template>

<style lang="scss">
.navigation {
  display: flex;
}
</style>
