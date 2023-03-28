<template>
  <v-app class="page_backgroud">
    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {};
  },
};
</script>

<style scoped>
.page_backgroud {
  background-color: whitesmoke;
  min-height: 100vh;
}

.container {
  width: 100vw !important;
  margin: 0;
}
</style>
