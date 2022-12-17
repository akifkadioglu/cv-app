<template>
  <div>
    <v-btn
      @click="isSettingOpen = !isSettingOpen"
      class="settings"
      icon
      color="primary"
      large
      depressed
      fab
    >
      <v-icon>mdi-cog-outline</v-icon>
    </v-btn>
    <transition name="fade" mode="out-in">
      <v-btn
        v-if="isSettingOpen"
        @click="changeMode"
        class="mode"
        icon
        large
        depressed
        fab
      >
        <v-icon>mdi-weather-night</v-icon>
      </v-btn>
    </transition>
    <transition name="fade" mode="out-in">
      <v-btn
        v-if="isSettingOpen"
        @click="changeLanguage"
        class="translate"
        icon
        large
        depressed
        fab
      >
        <v-icon>mdi-translate</v-icon>
      </v-btn>
    </transition>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isSettingOpen: false,
    };
  },
  methods: {
    changeLanguage() {
      this.$i18n.locale = this.$i18n.locale == "tr" ? "en" : "tr";
    },
    changeMode() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
    },
  },
};
</script>
<style scoped>
.settings {
  position: fixed;
  bottom: 45px;
  right: 20px;
}
.translate {
  position: fixed;
  bottom: 135px;
  right: 20px;
}
.mode {
  position: fixed;
  bottom: 225px;
  right: 20px;
}
</style>
