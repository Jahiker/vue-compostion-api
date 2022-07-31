<template>
  <div>FullName: {{ fullName }}</div>
</template>

<script>
import { ref, computed } from "vue";

  export default {
    setup() {
      const firstName = ref("Jahiker");
      const lastName = ref("Rojas");

      const fullName = computed(() => {
        return `${firstName.value} ${lastName.value}`;
      });      

      return {
        firstName,
        lastName,
        fullName
      };
    }
  }
</script>

<!-- <script setup>
import { ref, computed } from "vue";


const firstName = ref("Jahiker");
const lastName = ref("Rojas");

const fullName = computed(() => {
  return `${firstName.value} ${lastName.value}`;
});


</script> -->
