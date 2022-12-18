<template>
  <div class="resume-page text-center">
    <div align="center">
      <img src="@/assets/cv.png" rel="preload" />
    </div>

    <Back />
  </div>
</template>

<script>
import Back from "../components/Back.vue";
export default {
  components: { Back },
};
</script>

<style scoped>
.resume-page {
  height: 100vh;
  justify-content: center;
  align-items: center;
  display: grid;
}

img {
  max-height: 1024px;
  max-width: 100%;
}
</style>
