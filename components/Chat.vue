<template>
  <div class="chat">
    <div v-for="message in messages" :key="message.id" class="message">
      {{ message.text }}
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const messages = ref([
  { id: 1, text: 'Hello!' },
  { id: 2, text: 'How can I help you today?' },
  // Add more messages as needed
])
</script>

<style scoped>
.chat {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.message {
  padding: 0.5rem;
  background-color: #f0f0f0;
  border-radius: 4px;
}
</style>
