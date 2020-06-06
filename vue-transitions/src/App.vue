<template>
  <div id="app">
    <Index />
    <listTransition />
  </div>
</template>

<script>
import Index from "./components/index.vue";
import listTransition from "./components/listTransition.vue";
export default {
  name: "App",
  components: {
    Index,
    listTransition
  }
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
