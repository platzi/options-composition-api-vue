<template>
  <div>Fullname: {{ fullName }}</div>
</template>

<script>
import { ref, computed } from "vue";

export default {
  setup() {
    const firstName = ref("Diana");
    const lastName = ref("Martinez");

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    return {
      fullName,
    };
  },
};
</script>
