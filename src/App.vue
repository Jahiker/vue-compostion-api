<template>
  <Home first-name="Pili" last-name="Rojas" />
</template>

<script>
  import Home from "./components/Home.vue";
  import { provide } from "vue";

  export default {
    name: "App",
    components: {
      Home,
    },
    setup() {
      provide("username", "PiliLili");
    }
  }
</script>