<template>
  <h1
    class="mt-16 text-2xl tracking-tighter text-zinc-800 sm:text-3xl font-bold"
  >
    Articles
  </h1>
  <p class="mt-6 text-base text-zinc-600 max-w-2xl">
    Here are some of my writeups you might find interesting
  </p>
  <div class="mt-10 pb-5 -mx-4 space-y-4">
    <ul
      v-for="(item, index) in articles"
      :key="index"
      class="flex p-4 rounded-sm gap-2 text-[#27272a] hover:bg-zinc-50 font-normal items-center border-b"
    >
      <li>
        <a target="_blank" :href="item.link" class="group">
          <p v-if="item.name" class="font-semibold text-2xl">
            {{ item.name }}
          </p>
        </a>
      </li>
    </ul>
  </div>
</template>

<script setup>
const articles = [
  {
    name: "Understanding file access permissions in Unix-like systems",
    link: "https://dev.to/ize/understanding-file-access-permissions-in-unix-like-systems-2ckp",
    via: "dev.to",
  },
];
</script>
