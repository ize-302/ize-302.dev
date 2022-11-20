<template>
  <div>
    <Header />
    <div class="container mx-auto max-w-2xl px-4 md:px-0">
      <Hello />
      <Projects />
    </div>
    <Footer />
  </div>
</template>

<script>
import Hello from "./components/Hello.vue";
import Projects from "./components/Projects.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  components: { Hello, Projects, Header, Footer },
  name: "App",
};
</script>
