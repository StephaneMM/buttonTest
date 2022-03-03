<template>
  <div class="img-container">
    <img :src="icon" alt="search icon" width="30" height="30" />
  </div>
</template>

<script>
export default {
  name: "Icon",
  props: {
    icon: {
      default: "search-svgrepo-com.svg",
      type: String,
    },
  },
};
</script>

<style scoped>
</style>
