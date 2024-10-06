<template>
  <div class="history-chat">
    <h2>{{ chatTitle }}</h2>
    <div v-for="message in messages" :key="message.id" class="message">
      {{ message.text }}
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const chatTitle = ref('History Chat Title')
const messages = ref([
  { id: 1, text: 'This is a historical message.' },
  { id: 2, text: 'Another historical message.' },
  // Add more historical messages as needed
])
</script>

<style scoped>
.history-chat {
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
