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

    <transition
      name="fade"
      mode="out-in"
      v-for="(item, index) in settings"
      :key="index"
    >
      <v-btn
        v-if="isSettingOpen"
        @click="item.func"
        class="item"
        :style="'bottom:' + (120 + index * 50) + 'px'"
        icon
        large
        depressed
      >
        <v-icon>{{ item.icon }}</v-icon>
      </v-btn>
    </transition>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isSettingOpen: false,
      settings: [
        {
          icon: "mdi-weather-night",
          func: this.changeMode,
        },
        {
          icon: "mdi-translate",
          func: this.changeLanguage,
        },
      ],
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
.item {
  position: fixed;
  right: 30px;
}
</style>
