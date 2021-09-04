<template>
  <div class="home">
    <HelloWorld msg="barakhov.github.io" />
    <img alt="Vue logo" src="../assets/hackerman.jpg" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
};
</script>

<style scoped>
img {
  margin: 0 auto;
  max-width: 250px;
}
</style>
