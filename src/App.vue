<script setup>
import Logo from "./components/Logo.vue";
</script>

<template>
  <header>
    <div class="wrapper">
      
      <Logo msg="kappeskimchi" />
    </div>
  </header>

  <main></main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    /* place-items: center; */
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
