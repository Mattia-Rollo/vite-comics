<template>
  <div :key="index" class="card">
    <a href="#">
      <img :src="src" :alt="title" />
      <div>{{ title }}</div>
    </a>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["src", "title"],
};
</script>

<style lang="scss" scoped>
h1 {
  color: antiquewhite;
  background-color: aqua;
}
</style>
