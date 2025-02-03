<template>
  <div class="min-h-screen bg-white py-16 sm:py-32">
    <div class="container lg:mx-auto max-w-6xl px-5 md:px-10">
      <Introduction />
      <br />
      <work-experience />
      <br />
      <tools />
      <br />
      <projects />
      <!-- <articles /> -->
    </div>
  </div>
</template>

<script>
import Introduction from "./components/Introduction.vue";
import Projects from "./components/Projects.vue";
import Articles from "./components/Articles.vue";
import Tools from "./components/Tools.vue";
import WorkExperience from "./components/WorkExperience.vue"

export default {
  components: { Introduction, Projects, Articles, Tools, WorkExperience },
  name: "App",
};
</script>
