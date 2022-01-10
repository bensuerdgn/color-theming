<template>
  <div class="app"><Home /></div>
</template>

<script>
import Home from "./view/Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-family: Montserrat,sans-serif;
  outline: none;
  text-decoration: none;
}
</style>
