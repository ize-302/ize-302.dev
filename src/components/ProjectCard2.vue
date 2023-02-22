<template>
  <div class="p-4 rounded-md gap-24 text-gray-400 font-normal items-center">
    <a :href="item.link.url" target="_blank">
      <img class="object-cover h-48 w-full rounded-md mb-6" :src="item.image" />
    </a>
    <div class="">
      <p v-if="item.name" class="text-white font-normal text-sm mb-2">
        {{ item.name }}
      </p>
      <p v-if="item.description" class="text-sm">
        {{ item.description }}
      </p>
      <a
        :href="item.link.url"
        class="group mt-5 flex items-center gap-2 text-sm text-white"
        target="_blank"
        >{{ item.link.name }}
        <span class="material-symbols-outlined text-sm group-hover:opacity-60"
          >arrow_right_alt</span
        ></a
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectCard2",
  props: ["item"],
};
</script>
