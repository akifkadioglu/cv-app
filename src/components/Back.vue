<template>
  <div>
    <div class="back-item">
      <v-btn
        @click="$router.back()"
        icon
        large
        depressed
        fab
        class="fab-item"
        color="error"
      >
        <v-icon>mdi-arrow-left</v-icon>
      </v-btn>
    </div>
    <div class="show-back-item">
      <img
        class="show-settings"
        v-if="$i18n.locale == 'en'"
        src="@/assets/back-en.png"
        width="200px"
        rel="preload"
      />
      <img
        class="show-settings"
        v-else
        src="@/assets/back-tr.png"
        width="200px"
        rel="preload"
      />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.back-item {
  position: fixed;
  left: 20px;
  bottom: 45px;
  z-index: 1;
}
.show-back-item {
  position: fixed;
  left: 5px;
  bottom: 60px;
  z-index: 0;
}
</style>
