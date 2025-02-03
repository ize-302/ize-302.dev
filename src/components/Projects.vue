<template>
  <h1 class="mt-16 text-2xl tracking-tighter text-zinc-800 font-bold">
    Personal projects
  </h1>
  <p class="mt-2 text-base text-zinc-600 max-w-2xl">
    These are my favourite personal projects:
  </p>
  <div class="mt-5 pb-5 -mx-4 flex flex-wrap">
    <div v-for="(item, index) in personalprojects" :key="index" class="p-5" :class="item.type == 'banner'
      ? `w-full h-72 my-4 rounded-lg border border-zinc-200 text-black relative overflow-hidden flex items-start md:items-center flex-col md:flex-row`
      : 'w-full sm:w-1/2 lg:w-1/3'
      ">
      <div class="group block" :class="item.type === 'banner' ? 'w-full md:w-1/2 md:px-4' : 'w-full'">
        <p v-if="item.name" :class="`${item.type == 'banner' ? 'text-md md:text-2xl' : 'text-md'
          }`" class="font-semibold mb-2">
          {{ item.name }}
        </p>
        <p :class="`${item.type == 'banner'
          ? 'text-sm md:text-lg text-gray-300'
          : 'text-md'
          }`" v-if="item.description" class="text-zinc-500">
          {{ item.description }}
        </p>
        <div class="text-sm mt-2 flex items-center flex-wrap gap-1">
          <span class="bg-zinc-100 text-zinc-600 rounded-md py-0.5 px-1.5" v-for="tag in item.tags">{{ tag }}</span>
        </div>

        <a target="_blank" :href="item.link.url"
          class="relative z-10 mt-6 flex items-center text-sm font-medium text-zinc-400 transition group-hover:text-teal-500">
          <Icon icon="mdi:link-variant" class="h-4 w-4" />
          <span class="ml-1">{{ item.link.name }}</span>
        </a>
      </div>
      <div v-if="item.type == 'banner'" class="relative w-full flex items-center justify-center md:w-1/2 h-full">
        <img width="100%" class="absolute top-4 md:top-0 w-full rounded-md" :alt="item.name"
          :src="getImageUrl(item.thumbnail)" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { Icon } from '@iconify/vue';

const getImageUrl = (image) => {
  return new URL(`../assets/${image}`, import.meta.url);
};

const personalprojects = [
  {
    name: "🐈 thecatapi-py-sdk",
    description: "Python wrapper for making secure requests to TheCatAPI",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/thecatapi-py-sdk",
    },
    tags: ['Python']
  },
  {
    name: "🚗 car-rental-service",
    description:
      "An API service for a car rental platform. Built using python, fastapi, and Postgresql.",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/car-rental-service",
    },
    tags: ['Python', 'FastAPI', 'Postgresql']
  },
  {
    name: "🍞 Bunsoir",
    description:
      "Quickly setup Bun-based backend application with little development configuration",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/bunsoir",
    },
    tags: ['TypeScript', 'Shell script', 'Bunjs']
  },
  {
    name: "😎 gitmo",
    description: "Add appropriate emoji to your commit messages based on conventional commits specification",
    icon: "mood",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/gitmo",
    },
    tags: ['TypeScript', 'Shell script', 'Nodejs']
  },
  {
    name: "👮🏽 pkg-police",
    description:
      "A command-line utility that enumerates utilized and unused packages within a project.",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/pkg-police",
    },
    tags: ['Javascript']
  },

  {
    name: "🔄 env-sync",
    description:
      "env-sync automates the process of syncing and saving examples of all your env files",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/env-sync",
    },
    tags: ['Javascript']
  },

  {
    name: "🔖 Cmd+B",
    type: "banner",
    description:
      "A beautiful and accessible bookmark manager for your chrome browser",
    link: {
      name: "Chrome webstore",
      url: "https://chromewebstore.google.com/detail/cmd+b/flfoebhhngbkkmkicienbmbnafafodae",
    },
    thumbnail: "cmdb.png",
    tags: ['Javascript', 'Chrome API']
  },
];
</script>
