<template>
  <div class="py-10">
    <h1 class="text-4xl font-extrabold">Adavize Hassan</h1>
    <article class="mt-10">
      <div class="m-auto flex flex-col gap-4 leading-7 text-gray-600">
        <p>Hi, I am Adavize-</p>
        <p>
          I love JavaScript and Open Souce. Particularly, I have a passion for
          developing intuitive user interfaces for a snappy and delightful web
          experience.
        </p>
        <p>
          I currently work at
          <a
            class="text-black border-b border-gray-300"
            target="_blank"
            href="https://www.trysend.com/"
            >Send Shipping</a
          >
          as a Frontend Engineer.
        </p>
      </div>
    </article>
    <div class="border-t border-gray-200 w-20 my-10" />
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
  name: "HelloWorld",
  data() {
    return {
      message: "hi",
      opensourceprojects,
      browsertools,
      webapps,
      apis,
      latest,
    };
  },
  components: {
    ProjectCard,
  },
};
</script>
