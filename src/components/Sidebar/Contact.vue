<template>
  <div>
    <hr class="rounded" />
    <v-list-item>
      <v-list-item-content style="text-align: center">
        <h5>{{ $t("contact-me") }}</h5>
      </v-list-item-content>
    </v-list-item>
    <v-list-item
      v-for="(item, index) in contact"
      :key="index"
      link
      @click="goLink(item.link)"
    >
      <v-list-item-icon>
        <v-icon>{{ item.icon }}</v-icon>
      </v-list-item-icon>
      <v-list-item-title>{{ item.title }}</v-list-item-title>
    </v-list-item>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contact: [
        {
          title: "Github",
          icon: "mdi-github",
          link: "https://github.com/akifkadioglu",
        },
        {
          title: "LinkedIn",
          icon: "mdi-linkedin",
          link: "https://www.linkedin.com/in/akif-kadioglu-88429a1b2/",
        },
        {
          title: "Twitter",
          icon: "mdi-twitter",
          link: "https://twitter.com/akifkadioglu",
        },
        {
          title: "Instagram",
          icon: "mdi-instagram",
          link: "https://instagram.com/akifkadioglu",
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

<style></style>
