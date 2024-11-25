<template>
  <div class="mx-0 sm:mx-0 flex flex-col">
    <div class="flex flex-col sm:flex-row  sm:items-center gap-3">
        <img
          alt="Profile Picture"
          loading="lazy"
          width="80"
          height="80"
          decoding="async"
          data-nimg="1"
          class="rounded-full"
          style="color: transparent"
          src="../assets/dp.png"
        />
        <div>
          <h1 class="text-3xl sm:text-4xl font-bold tracking-tight">
            hi, Adavize here 👋 
          </h1>
          <p class="text-zinc-400">Fullstack Software developer from Nigeria 🇳🇬 </p>
        </div>
    </div>
   

    <p class="text-zinc-600 mt-6 text-md max-w-2xl font-normal leading-normal">
      I like to create softwares that cater to both developers and end-users. 
    </p>

    <div class="mt-6 flex items-center gap-6">
      <button @click="() => openResume()" class="hover:bg-transparent hover:text-zinc-900 border border-zinc-900 bg-zinc-900 text-white flex items-center gap-1 px-3 py-1 rounded-md">Resume  <Icon icon="material-symbols:file-save-sharp"  class="h-4 w-4" /></button>
      <a
        :href="item.url"
        target="_blank"
        rel="noreferrer noopener"
        v-for="item in socials">
        <Icon :icon="item.icon"  class="h-6 w-6 text-zinc-900 hover:scale-105 transition-all" />
      </a>
    </div>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue';

export default {
  name: "Introduction",
  data() {
    return {
      socials: [
        {
          name: 'github',
          url: 'https://github.com/ize-302',
          icon: 'cib:github'
        },
        {
          name: 'linkedin',
          url: 'https://linkedin.com/in/adavize-hassan',
          icon: 'cib:linkedin'
        },
        {
          name: 'gmail',
          url: 'mailto:adavize302@gmail.com',
          icon: 'cib:gmail'
        }
      ]
    }
  },
  methods: {
    openResume () {
      window.open("https://www.canva.com/design/DAGNEsIdZH4/NVfVOcK08QpwAmthL0WdlA/view?utm_content=DAGNEsIdZH4&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h5ade94348c", "_blank")
    }
  },
  components: {
    Icon
  }
};
</script>
