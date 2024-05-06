<template>
  <!-- Displaying the message -->
  <div>{{ message }}</div>
</template>

<script>
export default {
  // Prop to receive the initial message from the parent component
  props: ["initialMessage"],
  // Data to store and display the message
  data() {
    return {
      message: this.initialMessage,
    };
  },
  // Watcher to update the message when it changes in the parent component
  watch: {
    initialMessage(newMessage) {
      this.message = newMessage;
    },
  },
};
</script>
