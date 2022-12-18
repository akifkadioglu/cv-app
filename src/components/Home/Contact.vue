<template>
  <div>
    <div
      v-for="(item, index) in contact"
      :key="index"
      class="item"
      :style="'bottom:' + (120 + index * 50) + 'px'"
    >
      <transition name="fade" mode="out-in">
        <v-btn
          v-if="isContactsOpen"
          @click="goLink(item.link)"
          icon
          large
          depressed
        >
          <v-icon>{{ item.icon }}</v-icon>
        </v-btn>
      </transition>
    </div>
    <div>
      <v-btn
        @click="isContactsOpen = !isContactsOpen"
        icon
        large
        depressed
        fab
        class="fab-item"
        color="error"
      >
        <v-icon>mdi-account-settings-outline</v-icon>
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isContactsOpen: false,
      contact: [
        {
          title: "Mail",
          icon: "mdi-email-outline",
          link: "mailto: akifkadioglu@yaani.com",
        },
        {
          title: "Github",
          icon: "mdi-github",
          link: "https://github.com/akifkadioglu",
        },
        {
          title: "Whatsapp",
          icon: "mdi-whatsapp",
          link: "https://wa.me/+905558803528/?text=Merhaba!",
        },
        {
          title: "LinkedIn",
          icon: "mdi-linkedin",
          link: "https://www.linkedin.com/in/akif-kadioglu-88429a1b2/",
        },
      ],
    };
  },
  methods: {
    goLink(item) {
      window.open(item, "_blank");
    },
  },
};
</script>

<style scoped>
.fab-item {
  position: fixed;
  left: 20px;
  bottom: 45px;
}
.item {
  position: fixed;
  left: 30px;
}
</style>
