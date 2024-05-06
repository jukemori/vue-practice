<template>
  <div>Message: {{ message }}</div>
</template>

<script>
export default {
  props: ["initialMessage"],
  data() {
    return {
      message: this.initialMessage,
    };
  },
  watch: {
    initialMessage(newMessage) {
      this.message = newMessage;
    },
  },
};
</script>

<style scoped>
/* Add styles as needed */
</style>
