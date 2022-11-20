<template>
  <div>
    <h1 class="mb-4 text-2xl font-extrabold">Projects</h1>
    <p
      class="m-auto flex flex-col gap-4 leading-7 text-gray-400 font-light italic"
    >
      List of projects that I am proud to show-off
    </p>
    <!-- latest -->
    <p class="mt-10 font-semibold text-gray-600">Latest</p>
    <div class="py-5 -mx-4">
      <project-card v-for="(item, index) in latest" :item="item" :key="index" />
    </div>
    <!-- web apps -->
    <p class="mt-5 font-semibold text-gray-600">Web Apps</p>
    <div class="py-5 -mx-4 grid sm:grid-cols-2 gap-2">
      <project-card
        v-for="(item, index) in webapps"
        :item="item"
        :key="index"
      />
    </div>
    <!-- apis -->
    <p class="mt-5 font-semibold text-gray-600">APIs</p>
    <div class="py-5 -mx-4 grid sm:grid-cols-2 gap-2">
      <project-card v-for="(item, index) in apis" :item="item" :key="index" />
    </div>
    <!-- browser tools -->
    <p class="mt-5 font-semibold text-gray-600">Browser Tools</p>
    <div class="py-5 -mx-4 grid sm:grid-cols-2 gap-2">
      <project-card
        v-for="(item, index) in browsertools"
        :item="item"
        :key="index"
      />
    </div>
    <!-- open source contribution -->
    <p class="mt-5 font-semibold text-gray-600">Open-source Contributions</p>
    <div class="py-5 -mx-4 grid sm:grid-cols-2 gap-2">
      <project-card
        v-for="(item, index) in opensourceprojects"
        :item="item"
        :key="index"
      />
    </div>
  </div>
</template>

<script>
import ProjectCard from "./ProjectCard.vue";
import {
  latest,
  opensourceprojects,
  browsertools,
  webapps,
  apis,
} from "../projects";

export default {
  name: "Projects",
  components: {
    ProjectCard,
  },
  data() {
    return {
      opensourceprojects,
      browsertools,
      webapps,
      apis,
      latest,
    };
  },
};
</script>
