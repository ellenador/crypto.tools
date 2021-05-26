<template>
  <v-app dark>
    <v-app-bar dense :clipped-left="clipped" fixed app>
      <v-toolbar-title to="/" v-text="title" />
      <v-btn to="/" small text class="ml-9">Home</v-btn>
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      title: "Crypto.tools",
    };
  },
};
</script>

<style scoped>
.theme--dark .v-app-bar,
.v-navigation-drawer,
.v-list-item,
.v-footer {
  border: 1px rgb(170, 170, 170) !important;
  border-style: dashed double !important;
}
</style>