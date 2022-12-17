<template>
  <div>
    <v-list nav dense>
      <v-list-item>
        <v-list-item-content style="margin: auto">
          <v-list-item-avatar size="100">
            <img src="@/assets/profile.jpeg" />
          </v-list-item-avatar>
        </v-list-item-content>
      </v-list-item>
      <Contact />
    </v-list>
  </div>
</template>
<script>
import Contact from "./Sidebar/Contact.vue";
export default {
  components: {
    Contact,
  },
};
</script>
<style scoped>
hr.rounded {
  border-top: 2px solid #bbb;
  border-radius: 5px;
}
</style>
