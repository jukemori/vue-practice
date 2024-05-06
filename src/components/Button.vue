<template>
  <!-- Button for clicking -->
  <button @click="handleClick">Reverse Message</button>
</template>

<script>
export default {
  methods: {
    // Emitting a custom event when the button is clicked
    handleClick() {
      this.$emit("button-clicked");
    },
  },
};
</script>
