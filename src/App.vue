<template>
  <div class="container">
    <!-- Button to update the message -->
    <button @click="updateMessage">Update Message</button>

    <!-- Passes the 'message' data as a prop to the Message component-->
    <!-- Listens for the 'message-changed' event from the Message component-->
    <Message
      :initial-message="message"
      @message-changed="handleMessageChange"
    />

    <!-- Listens for the 'button-clicked' event from the Button component -->
    <Button @button-clicked="handleButtonClick" />

    <!-- Passes the 'reversedMessage' data as a prop to the ReversedMessage component -->
    <ReversedMessage :reversed-message="reversedMessage" />
  </div>
</template>

<script>
import Message from "./components/Message.vue"; // Importing the Message component
import Button from "./components/Button.vue"; // Importing the Button component
import ReversedMessage from "./components/ReversedMessage.vue"; // Importing the ReversedMessage component

export default {
  components: {
    Message,
    Button,
    ReversedMessage,
  },
  data() {
    return {
      message: "Hello Vue!", // Initial message data
      reversedMessage: "", // Data for the reversed message
    };
  },
  methods: {
    // Method to handle message change
    handleMessageChange(newMessage) {
      this.message = newMessage;
    },
    // Method to reverse the message
    handleButtonClick() {
      this.reversedMessage = this.message.split("").reverse().join("");
    },
    // Method to update the message
    updateMessage() {
      this.message = "Updated message";
    },
  },
};
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
