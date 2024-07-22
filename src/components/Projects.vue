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
          :alt="item.name"
          :src="getImageUrl(item.thumbnail)"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
const getImageUrl = (image) => {
  return new URL(`../assets/${image}`, import.meta.url);
};

const personalprojects = [
  {
    name: "📗 addressbook-cli",
    description:
      "A CLI app for managing contact addresses. Built with Python, Typer and sqlite3",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/addressbook-cli",
    },
  },
  {
    name: "🧭 border-ng-js",
    description:
      "An NPM package to check if a provided coordinate falls within the borders of Nigeria",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/border-ng-js",
    },
  },
  {
    name: "🍞 Bunsoir",
    description:
      "Quickly setup Bun-based backend application with little development configuration",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/bunsoir",
    },
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
  },
  {
    name: "🚗 car-rental-service",
    description:
      "An API service for a car rental platform. Built using python, fastapi, and Postgresql.",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/car-rental-service",
    },
  },

  {
    name: "🌐 EnvBadge",
    description:
      "Open-source solution for identifying your current web environment at a glance.",
    link: {
      name: "Live app",
      url: "https://envbadge.vercel.app",
    },
  },
  {
    name: "🔄 env-sync",
    description:
      "env-sync automates the process of syncing and saving examples of all your env files",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/env-sync",
    },
  },
  {
    name: "🗺️ geo-ng",
    description:
      "Geo-ng is a python package that provides geographical information about States, LGAs and towns in Nigeria",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/geo-ng",
    },
  },
  {
    name: "🗓️ json-days",
    description:
      "A JSON data model for getting list of days in a specified year, quarter or month",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/json-days",
    },
  },
  {
    name: "🔌 Gravicon",
    description:
      "Figma plugin to retrieve and display favicon from any provided domain or URL",
    link: {
      name: "Try it out",
      url: "https://www.figma.com/community/plugin/1307231621622379453/gravicon",
    },
  },
  {
    name: "⚙ Manage repos",
    type: "banner",
    description: "Update & delete your github repositories easily",
    link: {
      name: "Live app",
      url: "https://manage-repos.vercel.app",
    },
    thumbnail: "manage-repos.png",
  },

  {
    name: "👮🏽 pkg-police",
    description:
      "A command-line utility that enumerates utilized and unused packages within a project.",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/pkg-police",
    },
  },
  {
    name: "⭐ RateSQ",
    description: "Web app for rating opening sequence of tv shows",
    link: {
      name: "Live app",
      url: "https://rate-sq.vercel.app/",
    },
  },
  {
    name: "🐈 thecatapi-py-sdk",
    description: "Python wrapper for making secure requests to TheCatAPI",
    link: {
      name: "Source code",
      url: "https://github.com/ize-302/thecatapi-py-sdk",
    },
  },
  {
    name: "😎 gh-emoji",
    description: "Use GitHub emojis from their API as an npm package",
    icon: "mood",
    link: {
      name: "Contrubution",
      url: "https://github.com/privatenumber/gh-emojis/commits?author=ize-302",
    },
  },
  {
    name: "📅  JSON-calendar",
    description: "A JSON data object that I used to display a calendar web UI",
    icon: "calendar_month",
    link: {
      name: "Contribution",
      url: "https://github.com/rxgx/json-calendar/commits?author=ize-302",
    },
  },
  {
    name: "🏦  nigerian-banks",
    description: "An API that provides Nigerian bank logos, slug and code.",
    icon: "corporate_fare",
    link: {
      name: "Contribution",
      url: "https://github.com/ichtrojan/nigerian-banks",
    },
  },
  {
    name: "🕉 nigerialogos",
    description: "High quality vector logos for Nigerian companies",
    icon: "category",
    link: {
      name: "Contribution",
      url: "https://github.com/PaystackHQ/nigerialogos/commits?author=ize-302",
    },
  },
];
</script>
