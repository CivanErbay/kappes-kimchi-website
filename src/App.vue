<script>
import { defineComponent } from "vue";
import ImgCarousel from "./components/ImgCarousel.vue";
import DividerTextContent from "./components/DividerTextContent.vue";
import Navigation from "./components/Navigation.vue";
import { ElConfigProvider } from "element-plus";

export default defineComponent({
  components: {
    ElConfigProvider,
  },
});
</script>

<template>
  <el-config-provider>
    <header>
      <Navigation></Navigation>
    </header>

    <main>
      <Landing></Landing>
      <DividerTextContent></DividerTextContent>
      <ImgCarousel></ImgCarousel>
    </main>
  </el-config-provider>
</template>

<style scoped>
header {
  line-height: 1.5;
  position: absolute;
  z-index: 1;
  width: 100%;
}

@media (min-width: 1024px) {
  header {
    display: flex;
  }
}

</style>
