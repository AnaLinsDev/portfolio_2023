<template>
  <div>
    <v-card
      class="pa-10 card card_skills"
      height="100px"
      color="transparent"
      elevation="0"
    >
    <Skills />
    </v-card>
    <v-card class="pa-10 card card_project" color="transparent" elevation="0">
      <Projects />
    </v-card>
    <v-card
      class="pa-10 card card_me"
      height="100px"
      color="transparent"
      elevation="0"
    >
    <Me />
    </v-card>
  </div>
</template>

<script>

import Projects from "@/components/Projects.vue";
import Skills from "@/components/Skills.vue";
import Me from "@/components/Me.vue";

export default {
  name: "Portfolio",

  components: [Projects, Skills, Me],
};
</script>

<style scoped>
.card {
  width: 100vw !important;
}
.card_project {
  background-color: rgb(46, 221, 186) !important;
}

.card_skills {
  background-color: whitesmoke !important;
}

.card_me {
  background-color: whitesmoke !important;
}
</style>
