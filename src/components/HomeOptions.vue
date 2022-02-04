<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
  <button ref="btn">Click!</button>
</template>

<script>
export default {
  props: {
    firstName: String,
    lastName: String,
  },
  inject: ["username"],
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
  },
  mounted() {
    console.log(this.$refs.btn);
  },
};
</script>
