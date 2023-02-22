<template>
  <a
    v-if="item.link"
    :href="item.link"
    target="_blank"
    class="group px-4 py-4 hover:bg-gray-900 rounded-md flex gap-4 text-gray-400 font-normal items-center"
  >
    <div v-if="item.icon">
      <span class="material-symbols-outlined">{{ item.icon }}</span>
    </div>
    <div class="">
      <p v-if="item.name" class="mb-1 text-gray-600 font-normal text-sm">
        {{ item.name }}
      </p>
      <p v-if="item.description" class="text-sm group-hover:text-gray-500">
        {{ item.description }}
      </p>
    </div>
  </a>
</template>

<script>
export default {
  name: "ProjectCard",
  props: ["item"],
};
</script>
