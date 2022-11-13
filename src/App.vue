<template>
  <div>
    <div class="flex justify-between px-4 md:px-10 py-8">
      <p class="font-sans font-bold">IZE-302</p>
      <div>menus</div>
    </div>
    <div class="container mx-auto max-w-2xl px-4 md:px-0">
      <hello-world />
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
export default {
  components: { HelloWorld },
  name: "App",
};
</script>
