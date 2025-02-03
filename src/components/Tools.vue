<template>
  <h1 class="mt-16 text-2xl tracking-tighter text-zinc-800 font-bold">
    Tech stack
  </h1>
  <div class="mt-6 flex flex-wrap items-center gap-10">
    <div v-for="item in tools" class="flex flex-col items-center gap-3">
      <Icon :icon="item.icon" class="h-8 w-8" />
      <p class="text-xs text-zinc-600">{{ item.name }}</p>
    </div>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue';

export default {
  name: "Tools",
  data() {
    return {
      tools: [{
        name: 'Figma',
        icon: 'logos:figma'
      },
      {
        name: 'Javascript',
        icon: 'logos:javascript'
      }, {
        name: 'Typescript',
        icon: 'logos:typescript-icon'
      }, {
        name: 'Vue',
        icon: 'logos:vue',
      }, {
        name: 'Nextjs',
        icon: 'logos:nextjs-icon',
      }, {
        name: 'Tailwindcss',
        icon: 'logos:tailwindcss-icon',
      }, {
        name: 'Nodejs',
        icon: 'logos:nodejs-icon',
      }, {
        name: 'Python',
        icon: 'logos:python',
      },
      {
        name: 'Postgres',
        icon: 'logos:postgresql',
      }, {
        name: 'Supabase',
        icon: 'logos:supabase-icon'
      }, {
        name: 'AWS',
        icon: 'logos:aws'
      }]
    }
  },
  components: {
    Icon
  }
};
</script>
