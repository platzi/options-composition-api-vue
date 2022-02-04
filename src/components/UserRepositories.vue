<template>
  <div>{{ user }} Repositories</div>
</template>

<script>
export default {
  props: {
    user: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      repositories: [], // 1
      filters: {}, // 3
      searchQuery: "", // 2
    };
  },
  computed: {
    filteredRepositories() {
      // 3
      return null;
    },
    repositoriesMatchingSearchQuery() {
      // 2
      return null;
    },
  },
};
</script>
