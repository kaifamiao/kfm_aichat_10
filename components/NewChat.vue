<template>
  <div class="new-chat">
    <button @click="startNewChat">New Chat</button>
  </div>
</template>

<script setup>
const startNewChat = () => {
  // Implement new chat logic
  console.log('Starting new chat')
}
</script>

<style scoped>
.new-chat {
  padding: 1rem;
}
</style>
