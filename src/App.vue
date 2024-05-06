<template>
  <div class="container">
    <Message
      :initial-message="message"
      @message-changed="handleMessageChange"
    />
    <Button @button-clicked="handleButtonClick" />
    <ReversedMessage :reversed-message="reversedMessage" />
    <button @click="updateMessage">Update Message</button>
  </div>
</template>

<script>
import Message from "./components/Message.vue";
import Button from "./components/Button.vue";
import ReversedMessage from "./components/ReversedMessage.vue";

export default {
  components: {
    Message,
    Button,
    ReversedMessage,
  },
  data() {
    return {
      message: "Hello Vue!",
      reversedMessage: "",
    };
  },
  methods: {
    handleMessageChange(newMessage) {
      this.message = newMessage;
    },
    handleButtonClick() {
      this.reversedMessage = this.message.split("").reverse().join("");
    },
    updateMessage() {
      console.log("Updating message", this.message);
      this.message = "Updated message";
      console.log("Message updated", this.message);
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
