<template>
  <div class="pt-10 md:pt-24">
    <div class="flex items-center mt-10 justify-between">
      <div class="text-3xl animate-pulse">⚡⚡⚡</div>
      <div class="flex items-center gap-4">
        <a
          href="https://github.com/ize-302"
          class="hover:opacity-70"
          target="_blank"
        >
          <github-icon />
        </a>
      </div>
    </div>
    <p class="text-gray-400 font-normal mt-10">
      I'm <span class="text-white">Adavize</span> a software developer and
      tinkerer.
    </p>

    <p class="text-gray-400 mt-4 max-w-lg font-normal leading-7">
      Currently, my focus is on constructing and delivering as many products as
      possible. Join me on this venture as I strive to achieve my objective, one
      product at a time 🤞
    </p>

    <a
      class="mt-8 flex items-center gap-1 text-yellow-500"
      href="mailto:adavizeozorku@gmail.com"
      >Shoot me a mail
      <span class="material-symbols-outlined text-sm"> arrow_outward </span></a
    >
  </div>
</template>

<script>
import GithubIcon from "./github";

export default {
  name: "Hello",
  components: { GithubIcon },
};
</script>
