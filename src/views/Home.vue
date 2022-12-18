<template>
  <div>
    <div class="mt-5 mb-5">
      <div class="text-center">
        <v-list-item-avatar size="200">
          <img src="@/assets/profile.jpeg" />
        </v-list-item-avatar>
      </div>

      <h1 class="text-center">{{ $t("header") }}</h1>
    </div>
    <div class="text text-center">
      {{ $t("which-stack") }}
    </div>
    <div class="divider" />
    <div class="buttons">
      <v-btn
        color="primary"
        text
        class="button"
        @click="isAccountsShowing = !isAccountsShowing"
        depressed
        >{{ $t("accounts") }}
      </v-btn>
      <v-btn
        color="error"
        text
        class="button"
        @click="isSettingsShowing = !isSettingsShowing"
        depressed
      >
        {{ $t("settings") }}
      </v-btn>
    </div>
    <div class="buttons" v-if="false">
      <v-btn text class="button" depressed>
        {{ $t("about-me") }}
      </v-btn>
      <v-btn text class="button" depressed>
        {{ $t("projects") }}
      </v-btn>
    </div>
    <div class="buttons">
      <v-btn text class="button" :to="{ name: 'Resume' }" depressed>
        {{ $t("resume") }}
      </v-btn>
    </div>
    <transition name="fade" mode="out-in">
      <img
        rel="preload"
        class="show-accounts"
        v-if="isAccountsShowing"
        src="@/assets/arrow.png"
        width="200px"
      />
    </transition>
    <transition name="fade" mode="out-in">
      <img
        rel="preload"
        class="show-settings"
        v-if="isSettingsShowing"
        src="@/assets/right.png"
        width="200px"
      />
    </transition>
    <Contact />
  </div>
</template>

<script>
import Contact from "../components/Home/Contact.vue";
export default {
  components: {
    Contact,
  },
  data() {
    return {
      isSettingsShowing: false,
      isAccountsShowing: false,
    };
  },
  name: "Home",
};
</script>
<style scoped>
img {
  z-index: 0;
}
.button {
  z-index: 1;
}
.text {
  font-size: 23px;
}

.divider {
  margin-top: 10px;
  height: 1px;
  background: linear-gradient(45deg, #e4bb68, #e06c75, #61afef);
}
.buttons {
  margin-top: 30px;
  display: flex;
  justify-content: space-around;
}
.show-accounts {
  position: fixed;
  left: 5px;
  bottom: 60px;
}
.show-settings {
  position: fixed;
  right: 55px;
  bottom: -35px;
}
</style>
