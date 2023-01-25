<template>
  <div>
    <swiper :options="swiperOptions">
      <swiper-slide
        style="display: flex; justify-content: center"
        v-for="(image, index) in images"
        :key="index"
      >
        <img class="swiper-img" :src="image" alt="slider image" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import SwiperClass, { Pagination } from "swiper";
import { Swiper, SwiperSlide } from "vue-awesome-swiper";

import "swiper/css";
import "swiper/css/pagination";
export default {
  data() {
    return {
      swiperOptions: {
        // options for the swiper
      },
      images: [
        "./kimchi1.jpg",
        "./kimchi5.jpg",
        "./kimchi6.jpg",
        "./kimchi8.jpg",
        "./kimchi22.jpg",
        "./kimchi24.jpg",
        "./kimchi_glas.jpg",
      ],
      components: {
        Swiper,
        SwiperSlide,
      },
      setup() {
        return {
          modules: [Pagination],
        };
      },
    };
  },
};
</script>

<style lang="scss">
.swiper-img {
  height: 600px;
  width: 450px;
  object-fit: cover;
  cursor: pointer;
}

</style>
