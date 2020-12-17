<template>
  <div id="app">
    <Vis />
  </div>
</template>

<script>
import Vis from "./components/Vis.vue";

export default {
  name: "App",
  components: {
    Vis,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
