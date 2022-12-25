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
      <div>
        <div>
          <h3>Willkommen</h3>
                <el-image style="width: 60vw; height: 60vh" src="./kimchi10.jpg" :fit="fit" />
        </div>
      </div>
      <DividerTextContent></DividerTextContent>
      <ImgCarousel></ImgCarousel>
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

main {
  animation-name: contentAnim;
  animation-duration: 1s;
  animation-delay: 3s;
  animation-fill-mode: forwards;
  opacity: 0;
}

@keyframes contentAnim {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
