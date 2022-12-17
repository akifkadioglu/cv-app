<template>
  <div>
    <div class="item" :style="'bottom:' + 90 + 'px'">asd</div>
    <div></div>
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

<style scoped>
.item {
  position: fixed;
  left: 20px;
}
</style>
