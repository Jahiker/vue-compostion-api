<template>
  <h1>{{ text }}</h1>
  <p>{{ counter }}</p>
  <p>{{ obj }}</p>
</template>

<script>
import { ref, reactive } from "vue";

  export default {
    setup() {
      const text = ref("Hola Vue");
      const counter = ref(0);
      const obj = reactive({
        counter: 0
      })

      setInterval(() => counter.value++, 1000);
      setInterval(() => obj.counter++, 1000);

      return {
        text,
        counter,
        obj
      }
    }
  }
</script>
