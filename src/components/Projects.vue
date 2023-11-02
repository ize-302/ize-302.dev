<template>
  <h1
    class="mt-16 text-2xl tracking-tighter text-zinc-800 sm:text-3xl font-bold"
  >
    Projects
  </h1>
  <p class="mt-6 text-base text-zinc-600 max-w-2xl">
    I've worked on many small projects over the years but these are my
    favorites. Most are open-source, so check out the code and contribute if you
    have ideas for improvement.
  </p>
  <div
    class="mt-10 pb-5 -mx-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4"
  >
    <div
      v-for="(item, index) in personalprojects"
      :key="index"
      class="flex p-4 rounded-sm gap-2 text-[#27272a] hover:bg-zinc-50 font-normal items-center"
    >
      <a target="_blank" :href="item.link.url" class="group">
        <p v-if="item.name" class="font-semibold text-md mb-2">
          {{ item.name }}
        </p>
        <p v-if="item.description" class="text-sm text-zinc-600">
          {{ item.description }}
        </p>

        <p
          class="relative z-10 mt-6 flex items-center text-sm font-medium text-zinc-400 transition group-hover:text-teal-500"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="h-4 w-4"
          >
            <path
              d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"
            ></path>
            <path
              d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"
            ></path>
          </svg>
          <span class="ml-2">{{ item.link.name }}</span>
        </p>
      </a>
    </div>
  </div>
</template>

<script>
import { personalprojects } from "../projects";

export default {
  name: "Projects",
  data() {
    return {
      personalprojects,
    };
  },
};
</script>
