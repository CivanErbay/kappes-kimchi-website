<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="kk-teaser">
    <img class="kk-teaser--img" src="../assets/photos/kimchi23.jpg" />
  </div>
</template>

<style scoped lang="scss">
.kk-teaser {
  width: 100%;

  &--img {
    height: 200px;
  }
}
</style>
