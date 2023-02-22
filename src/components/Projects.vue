<template>
  <div>
    <div class="flex items-center mb-4 mt-10 gap-5">
      <h1 class="text-white font-medium">Projects</h1>
      <div class="w-full border-b border-gray-800" />
    </div>
    <div
      class="pb-5 -mx-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-2"
    >
      <project-card2
        v-for="(item, index) in products"
        :item="item"
        :key="index"
      />
    </div>

    <!-- open source contribution -->
    <div class="flex items-center mb-5 mt-10 gap-4">
      <h1 class="text-white font-medium whitespace-nowrap">
        Open-source Contributions
      </h1>
      <div class="w-full border-b border-gray-800" />
    </div>
    <div class="-mx-4 grid sm:grid-cols-2 gap-6">
      <project-card
        v-for="(item, index) in opensourceprojects"
        :item="item"
        :key="index"
      />
    </div>
  </div>
</template>

<script>
import ProjectCard2 from "./ProjectCard2.vue";
import ProjectCard from "./ProjectCard.vue";
import { opensourceprojects, products } from "../projects";

export default {
  name: "Projects",
  components: {
    ProjectCard,
    ProjectCard2,
  },
  data() {
    return {
      opensourceprojects,
      products,
    };
  },
};
</script>
