<template>
  <div>{{ fullName }}</div>
</template>

<script>
import { computed, toRefs } from "vue";

  export default {
    props: {
      firstName: String,
      lastName: String
    },
    setup(props, context) {
    console.log("🚀 ~ file: Home.vue ~ line 14 ~ setup ~ context", context);
      
      const { firstName, lastName } = toRefs(props);

      const fullName = computed(() => {
        return `${firstName.value} ${lastName.value}`;
      });
      
      context.expose({
        fullName
      })

      return {
        fullName
      };
    }
  }
</script>
