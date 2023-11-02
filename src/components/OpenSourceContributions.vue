<template>
  <!-- open source contribution -->
  <div class="mt-10">
    <h1
      class="mt-16 text-2xl tracking-tighter text-zinc-800 sm:text-3xl font-bold"
    >
      Open-source contributions
    </h1>
    <p class="mt-6 text-base text-zinc-600 max-w-2xl">
      Here are some of open-source projects I have contributed to. It's not
      much, but it is honest work
    </p>
  </div>
  <div class="mt-10 -mx-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
    <a
      v-for="(item, index) in opensourcecontributions"
      :key="index"
      :href="item.link"
      target="_blank"
      class="group px-4 py-4 hover:bg-zinc-50 rounded-md flex flex-col gap-2 text-zinc-400 font-normal"
    >
      <div v-if="item.icon">
        <span
          class="material-symbols-outlined group-hover:text-teal-500 mb-2"
          >{{ item.icon }}</span
        >
      </div>
      <p v-if="item.name" class="text-zinc-600 font-semibold text-sm">
        {{ item.name }}
      </p>

      <p v-if="item.description" class="text-sm text-zinc-600">
        {{ item.description }}
      </p>
    </a>
  </div>
</template>

<script>
import { opensourcecontributions } from "../projects";

export default {
  name: "OpenSourceContributions",
  // props: ["item"],
  data() {
    return {
      opensourcecontributions,
    };
  },
};
</script>
