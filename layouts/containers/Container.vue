<template>
  <v-app>
    <v-main>
      <AppBar />
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
import AppBar from "@/layouts/containers/AppBar.vue";
export default {
  name: "Container",
  components: {
    AppBar,
  },
};
</script>
