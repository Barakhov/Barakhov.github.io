<template>
  <div class="about">
    <Hero msg="This is an about page" />
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
