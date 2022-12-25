<script>
import { defineComponent } from "vue";
import Logo from "./components/Logo.vue";
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
      <ImgCarousel></ImgCarousel>
      <DividerTextContent></DividerTextContent>
    </main>
  </el-config-provider>
</template>

<style scoped>
header {
  line-height: 1.5;
}

@media (min-width: 1024px) {
  header {
    display: flex;
  }
}
</style>
