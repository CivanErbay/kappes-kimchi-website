<template>
  <el-menu
    :default-active="activeIndex"
    class="navigation-wrapper"
    mode="horizontal"
    :ellipsis="false"
    @select="handleSelect"
    background-color="transparent"
    text-color="white"
    active-text-color="hsla(160, 100%, 37%, 1)"
  >
    <el-menu-item class="logo-item" index="0"
      ><Logo msg="kappeskimchi"
    /></el-menu-item>
    <div class="flex-grow" />
    <el-sub-menu index="1" class="sub-menu-wrapper">
      <template #title>kappes</template>
      <el-menu-item index="2-1">item one</el-menu-item>
      <el-menu-item index="2-2">journey</el-menu-item>
      <el-menu-item index="2-3">contact</el-menu-item>
    </el-sub-menu>
  </el-menu>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import Logo from "./Logo.vue";

const activeIndex = ref("1");
const handleSelect = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
</script>

<style lang="scss">
.flex-grow {
  flex-grow: 1;
}

.navigation-wrapper {
  &.el-menu--horizontal {
    flex-wrap: wrap;
    border: 0;

    @media (min-width: 1024px) {
      width: 100%;
    }
  }
}

.el-popper {
  background-color: #181818 !important;
}

.logo-item {
  pointer-events: none;
}

.sub-menu-wrapper div {
  font-size: 28px;
  animation-name: menuAnim;
  animation-duration: 1s;
  animation-delay: 3s;
  animation-fill-mode: forwards;
  opacity: 0;
}

@keyframes menuAnim {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
