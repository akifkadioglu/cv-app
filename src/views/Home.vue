<template>
  <div>
    <div class="mt-5">
      <h1 class="text-center">{{ $t("header") }}</h1>
    </div>
    <Contact />
  </div>
</template>

<script>
import Contact from "../components/Home/Contact.vue";
export default {
  components: {
    Contact,
  },
  name: "Home",
};
</script>
