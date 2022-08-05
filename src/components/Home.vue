<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
</template>

<script>
import { computed, toRefs, inject } from "vue";

  export default {
    props: {
      firstName: String,
      lastName: String
    },
    setup(props, context) {
    
      const { firstName, lastName } = toRefs(props);

      const fullName = computed(() => {
        return `${firstName.value} ${lastName.value}`;
      });

      const username = inject("username")
      console.log("🚀 ~ file: Home.vue ~ line 22 ~ setup ~ username", username)
      
      context.expose({
        fullName
      })

      return {
        fullName,
        username
      };
    }
  }
</script>
