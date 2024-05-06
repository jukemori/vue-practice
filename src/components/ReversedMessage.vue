<template>
  <div>Reversed Message: {{ reversedMessage }}</div>
  <div>Length of Reversed Message: {{ reversedMessageLength }}</div>
</template>

<script>
export default {
  props: ["reversedMessage"],
  computed: {
    reversedMessageLength() {
      return this.reversedMessage.length;
    },
  },
};
</script>

<style scoped>
/* Add styles as needed */
</style>
