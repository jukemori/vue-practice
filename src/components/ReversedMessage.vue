<template>
  <!-- Displaying the reversed message and its length -->
  <div>{{ reversedMessage }}</div>
  <div>Length: {{ reversedMessageLength }}</div>
</template>

<script>
export default {
  // Prop to receive the reversed message from the parent component
  props: ["reversedMessage"],
  computed: {
    reversedMessageLength() {
      // Computed property to calculate the length of the reversed message
      return this.reversedMessage.length;
    },
  },
};
</script>
