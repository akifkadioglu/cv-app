<template>
  <v-app>
    <v-main>
      <div class="container">
        <transition name="fade" mode="out-in">
          <router-view />
        </transition>
      </div>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Footer,
  },
  mounted() {
    setTimeout(function () {
      window.scrollTo(0, 1);
    }, 0);
  },
  data() {
    return {};
  },
};
</script>
<style>
.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
}
/* width */
::-webkit-scrollbar {
  width: 5px;
  border-radius: 20;
}
/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}
/* Handle */
::-webkit-scrollbar-thumb {
  background: #888;
}
/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555;
}
body {
  font-family: "Readex Pro";
}
.scroll {
  overflow-y: scroll;
}
.center {
  display: grid;
  place-items: center;
}
</style>
