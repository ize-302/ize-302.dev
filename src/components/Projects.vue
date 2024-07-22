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
  <div class="mt-10 pb-5 -mx-4 flex flex-wrap">
    <div
      v-for="(item, index) in personalprojects"
      :key="index"
      class="p-4"
      :class="
        item.type == 'banner'
          ? `w-full h-72 my-4 rounded-lg bg-zinc-800 text-white relative overflow-hidden flex items-start md:items-center flex-col md:flex-row`
          : 'w-full sm:w-1/2 lg:w-1/3'
      "
    >
      <a
        target="_blank"
        :href="item.link.url"
        class="group block"
        :class="item.type === 'banner' ? 'w-full md:w-1/2 md:px-4' : 'w-full'"
      >
        <p
          v-if="item.name"
          :class="`${
            item.type == 'banner' ? 'text-md md:text-2xl' : 'text-md'
          }`"
          class="font-semibold mb-2"
        >
          {{ item.name }}
        </p>
        <p
          :class="`${
            item.type == 'banner'
              ? 'text-sm md:text-lg text-gray-300'
              : 'text-sm'
          }`"
          v-if="item.description"
          class="text-zinc-600"
        >
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
      <div
        v-if="item.type == 'banner'"
        class="relative w-full flex items-center justify-center md:w-1/2 h-full"
      >
        <img
          width="100%"
          class="absolute top-4 md:top-0 w-full rounded-md"
          alt="ss"
          :src="`src/assets/${item.thumbnail}`"
        />
      </div>
    </div>
    <!-- <div
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
    </div> -->
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
