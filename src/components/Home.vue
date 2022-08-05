<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
  <button ref="btn">Click</button>
</template>

<script>
import { computed, toRefs, inject, ref, watch } from "vue";

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

      const username = inject("username");

      const btn = ref(null);

      console.log("🚀 ~ file: Home.vue ~ line 26 ~ setup ~ btn", btn.value);

      watch(btn, (valor) => {
        console.log("🚀 ~ file: Home.vue ~ line 30 ~ watch ~ valor", valor)
      })
      
      context.expose({
        fullName
      })

      return {
        fullName,
        username,
        btn
      };
    }
  }
</script>
