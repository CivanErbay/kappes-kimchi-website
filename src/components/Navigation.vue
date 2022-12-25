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
    <el-menu-item index="1">Processing Center</el-menu-item>
    <el-sub-menu index="2">
      <template #title>Workspace</template>
      <el-menu-item index="2-1">item one</el-menu-item>
      <el-menu-item index="2-2">item two</el-menu-item>
      <el-menu-item index="2-3">item three</el-menu-item>
      <el-sub-menu index="2-4">
        <template #title>item four</template>
        <el-menu-item index="2-4-1">item one</el-menu-item>
        <el-menu-item index="2-4-2">item two</el-menu-item>
        <el-menu-item index="2-4-3">item three</el-menu-item>
      </el-sub-menu>
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
</style>
