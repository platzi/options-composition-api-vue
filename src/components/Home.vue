<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
  <button ref="btn">Click!</button>
</template>

<script>
import { ref, toRefs, computed, watch, inject } from "vue";

export default {
  props: {
    firstName: String,
    lastName: String,
  },
  setup(props, { expose }) {
    const { firstName, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    const username = inject("username");

    expose({
      fullName,
    });

    const btn = ref(null);

    console.log(btn.value);

    watch(btn, (valor) => {
      console.log(valor);
    });

    return {
      fullName,
      username,
      btn,
    };
  },
};
</script>
