<template>
  <Home first-name="Diana" last-name="Martinez"></Home>
</template>

<script>
import Home from "@/components/HomeOptions.vue";
import { provide } from "vue";

export default {
  name: "App",
  components: {
    Home,
  },
  setup() {
    provide("username", "DianaNerd");
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
