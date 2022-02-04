<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
</template>

<script>
import { toRefs, computed, inject } from "vue";

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

    return {
      fullName,
      username,
    };
  },
};
</script>
