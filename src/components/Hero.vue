<template>
  <div>
    <h4>{{ msg }}</h4>
  </div>
</template>

<script>
export default {
  name: "Hero",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h4 {
  text-align: center;
}
</style>
