<template>
  <div class="home">
    <Hero msg="barakhov.github.io" />
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from "@/components/Hero.vue";

export default {
  name: "Home",
  components: {
    Hero,
  },
};
</script>
