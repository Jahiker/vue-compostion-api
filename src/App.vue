<template>
  <Home first-name="Pili" last-name="Rojas" otro="hola" />
</template>

<script>
  import Home from "./components/Home.vue";

  export default {
    name: "App",
    components: {
      Home,
    }
  }
</script>