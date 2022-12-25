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

<style scoped lang="scss">
.logo {
  display: flex;
  //padding: 400px;
  position: relative;
  animation-name: logoAnim;
  animation-duration: 3s;
  animation-delay: 0;
}

h1 {
  font-weight: 500;
  font-size: 1.6rem;

  @media (min-width: 1024px) {
    font-size: 2.6rem;
  }
}

h2 {
  font-size: 18px;
  font-weight: bold;
  margin-top: -7px;
}

@keyframes logoAnim {
  0% {
    padding: 400px;
  }
  50% {
    padding: 400px;
  }
  100% {
    padding: 0px;
  }
}
</style>
