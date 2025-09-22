<template>
  <div class="mx-0 sm:mx-0 flex flex-col">
    <div class="flex flex-col sm:flex-row sm:items-center gap-3">
      <div>
        <h1 class="text-3xl sm:text-4xl font-bold mb-2 tracking-tight">
          Adavize Hassan 👋
        </h1>
        <p class="text-zinc-400 gap-1 flex items-center">
          <Icon icon="material-symbols:location-on-outline" class="h-6 w-6" />
          Lagos, Nigeria 🇳
        </p>
      </div>
    </div>

    <p class="text-zinc-600 mt-6 text-lg max-w-2xl font-normal leading-normal">
      I’m a Fullstack Developer with 6+ years of experience building and scaling
      customer-facing applications. I enjoy working across the stack—whether
      crafting smooth user experiences or designing robust backend systems
    </p>

    <div class="mt-6 flex items-center gap-6">
      <a
        :href="item.url"
        :key="item.name"
        target="_blank"
        rel="noreferrer noopener"
        v-for="item in socials"
      >
        <Icon
          :icon="item.icon"
          class="h-6 w-6 text-zinc-900 hover:scale-105 transition-all"
        />
      </a>
    </div>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";

export default {
  name: "Introduction",
  data() {
    return {
      socials: [
        {
          name: "github",
          url: "https://github.com/ize-302",
          icon: "cib:github",
        },
        {
          name: "linkedin",
          url: "https://linkedin.com/in/adavize-hassan",
          icon: "cib:linkedin",
        },
        {
          name: "gmail",
          url: "mailto:adavize302@gmail.com",
          icon: "cib:gmail",
        },
      ],
    };
  },
  methods: {
    openResume() {
      window.open(
        "https://www.canva.com/design/DAGNEsIdZH4/NVfVOcK08QpwAmthL0WdlA/view?utm_content=DAGNEsIdZH4&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h5ade94348c",
        "_blank",
      );
    },
  },
  components: {
    Icon,
  },
};
</script>
