<template>
  <div class="kk-swiper">
    <div class="kk-swiper--wrapper">
      <h2 class="kk-swiper--headline">Einsicht in unsere Fertigung</h2>
      <swiper
        v-show="imgAccVal >= 11"
        :modules="[Navigation]"
        navigation
        :loop="true"
        :pagination="{ clickable: true }"
      >
        <swiper-slide
          style="display: flex; justify-content: center"
          v-for="(image, index) in images"
          :key="index"
        >
          <img
            class="swiper-img"
            :src="image"
            loading="lazy"
            alt="slider image"
            @load="triggerLoadVal()"
          />
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>
<script setup>
import { ref, defineEmits } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation } from "swiper";
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";

const images = ref([
  "./kimchi1.jpg",
  "./kimchi5.jpg",
  "./kimchi6.jpg",
  "./kimchi8.jpg",
  "./kimchi22.jpg",
  "./kimchi24.jpg",
  "./kimchi_blank.jpg",
  "./kimchi_paar.jpg",
  "./hanna_civan.jpg",
]);

let imgAccVal = ref(0);

const emit = defineEmits(["imgloaded"]);

const triggerLoadVal = () => {
  imgAccVal.value++;
  if (imgAccVal.value >= 11) {
    emit("imgloaded", true);
  }
};
</script>

<style lang="scss">
.swiper-img {
  height: 350px;
  width: 230px;
  object-fit: cover;
  cursor: pointer;
  border: 5px #181818 solid;
  border-radius: 5px;
  

  @media screen and (min-width: 768px) {
    border: 10px solid;
    flex-direction: row;
    height: 650px;
    width: 430px;
  }
}

.kk-swiper {
  width: 100%;
  display: flex;
  justify-content: center;
  margin: 35px 0;

  @media screen and (min-width: 768px) {
    margin: 60px 0;
  }

  &--headline {
    display: flex;
    justify-content: center;
    padding: 20px 0 23px;
    font-size: 15px;
    font-weight: bold;

    @media screen and (min-width: 768px) {
      font-size: 24px;
    }
  }
}

.swiper-button-next:after,
.swiper-button-prev:after {
  color: #181818;
}

.kk-swiper--wrapper {
  width: 100%;

  @media screen and (min-width: 768px) {
    width: 50%;
  }
}
</style>
