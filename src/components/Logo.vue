<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="logo green">
    <h2>김치</h2>
    <h1>{{ msg }}</h1>
  </div>
</template>

<style scoped>
.logo {
  display: flex;
}

h1 {
  font-weight: 500;
  font-size: 2.6rem;
}

h2 {
  font-size: 2.2rem;
  font-weight: bold;
}

.logo h1,
.logo h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .logo h1,
  .logo h3 {
    text-align: left;
  }
}
</style>
