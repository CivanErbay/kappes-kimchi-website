<script>
import { defineComponent } from "vue";
import Logo from "./components/Logo.vue";
import ImgCarousel from "./components/ImgCarousel.vue";
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
      <div class="wrapper">
        <Logo msg="kappeskimchi" />
      </div>
    </header>

    <main>
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

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
