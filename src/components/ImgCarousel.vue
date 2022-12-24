<script setup>
const imagePaths = [
  "./kimchi1.jpg",
  "./kimchi5.jpg",
  "./kimchi6.jpg",
  "./kimchi8.jpg",
  "./kimchi22.jpg",
  "./kimchi24.jpg",
  "./kimchi21.jpg",
];
</script>

<template>
  <el-row class="img-carousel" justify="center">
    <el-carousel arrow="always" :autoplay="false">
      <el-carousel-item v-for="imageSrc in imagePaths">
        <img class="img-item" :src="imageSrc" alt="" />
      </el-carousel-item>
    </el-carousel>
  </el-row>
</template>

<style lang="scss">
.img-carousel {
  margin-top: 80px;
}

.img-item {
  height: 400px;
  object-fit: cover;
  width: 100%;

  @media (min-width: 1024px) {
    height: 650px;
  }
}

.el-carousel {
  width: 100%;

  @media (min-width: 1024px) {
    width: 50%;
  }

  &__arrow {
    bottom: 0 !important;
    top: unset !important;
  }

  &__button {
    display: none !important;
    width: 10px !important;
  }

  &__indicator {
    margin: 0 5px;

    &s {
      width: 70%;
      display: flex;
      justify-content: space-around;
    }
  }

  &__container {
    height: 400px !important;

    @media (min-width: 1024px) {
      height: 650px !important;
    }
  }
}
</style>
