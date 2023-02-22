<template>
  <div class="min-h-screen bg-black">
    <div class="container lg:mx-auto max-w-5xl px-5 md:px-10">
      <Hello />
      <Projects />
      <Footer />
    </div>
  </div>
</template>

<script>
import Hello from "./components/Hello.vue";
import Projects from "./components/Projects.vue";
import Footer from "./components/Footer.vue";

export default {
  components: { Hello, Projects, Footer },
  name: "App",
};
</script>
