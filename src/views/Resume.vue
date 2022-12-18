<template>
  <div class="resume-page text-center">
    <img src="@/assets/cv.png" width="100%" />
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
}
</style>
