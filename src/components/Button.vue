<template>
  <button @click="handleClick">Reverse Message</button>
</template>

<script>
export default {
  methods: {
    handleClick() {
      this.$emit("button-clicked");
    },
  },
};
</script>

<style scoped>
/* Add styles as needed */
</style>
