<template>
  <v-card class="ma-10" color="transparent" elevation="0">
    <h1 class="mb-10">Projeto " {{ projects[model].name }} "</h1>
    <v-carousel v-model="model">
      <v-carousel-item
        v-for="(item, i) in projects"
        :key="i"
        :src="item.image"
        reverse-transition="fade-transition"
        transition="fade-transition"
      ></v-carousel-item>
    </v-carousel>
    <v-card class="mt-10" color="transparent" elevation="0">
      <h1>
        <span>
          <a :href="projects[model].link" target="_blank"> Link GitHub</a>
        </span>
        <br />
        Skills usadas: {{ projects[model].categories }}
      </h1>
    </v-card>
  </v-card>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "Projects",

  data() {
    return {
      model: 0,
    };
  },

  computed: {
    ...mapState("project", {
      projects: (state) => state.projects,
    }),

    currentProject() {
      return this.projects[model] !== undefined
        ? this.projects[model]
        : { name: "" };
    },
  },
};
</script>

<style>
a {
  text-decoration: none;
  color: rgb(5, 22, 175) !important;
}
a:hover {
  color: rgb(246, 175, 24) !important;
}
</style>
