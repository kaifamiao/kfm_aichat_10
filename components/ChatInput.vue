<template>
  <div class="chat-input">
    <SelectList />
    <textarea v-model="message" placeholder="Type your message..."></textarea>
    <button @click="sendMessage">Send</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import SelectList from './SelectList.vue'

const message = ref('')

const sendMessage = () => {
  console.log('Sending message:', message.value)
  // Implement send message logic
  message.value = ''
}
</script>

<style scoped>
.chat-input {
  display: flex;
  gap: 1rem;
  padding: 1rem;
  background-color: #f0f0f0;
}

textarea {
  flex: 1;
  min-height: 50px;
}
</style>
