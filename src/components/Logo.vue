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
    <!-- <h2>배추김치</h2> -->

    <!--    <h2>KIMCHI</h2> -->

    <img class="logo--img" src="../assets/kappes-black-outline.png" alt="" />
    <h1>{{ msg }}</h1>
  </div>
</template>

<style scoped lang="scss">
.logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: absolute;
  z-index: 3;
  top: 220px;
  padding: 3px 12px 0px;
  background-color: white;
  width: 58%;
  right: 11px;

  &--img {
    height: 115px;
  }

  @media (min-width: 1024px) {
    animation-name: logoAnim;
    animation-duration: 3s;
    animation-delay: 1.5s;
    animation-fill-mode: forwards;
    transform: translateY(-125%);
    background-color: rgba(0, 0, 0, 0);
    width: fit-content;
    left: 40%;
    top: 75%;
    padding: 20px 40px 20px;
  }
}

h1 {
  font-weight: 500;
  font-size: 2.6rem;
  font-family: "Righteous", cursive;
  color: #181818;
  font-weight: 600;

  @media (min-width: 1024px) {
    font-size: 2.6rem;
  }
}

h2 {
  font-size: 24px;
  /* font-weight: bold;
  margin-top: 7px; */
  animation-name: logoAnimMobile;
  animation-duration: 3s;
  animation-delay: 0;
  animation-fill-mode: forwards;

  @media (min-width: 1024px) {
    font-size: 36px;
    /* font-weight: bold; */
    /* margin-top: 11px; */
  }
}

@keyframes logoAnimMobile {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes logoAnim {
  0% {
    left: 40%;
    top: 75%;
  }
  20% {
    background-color: rgb(255, 255, 255, 0);
  }
  100% {
    left: 0;
    top: 50%;
    background-color: rgb(255, 255, 255, 1);
  }
}
</style>
