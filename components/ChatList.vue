<template>
  <ul class="chat-list">
    <li v-for="chat in chats" :key="chat.id" @click="selectChat(chat)">
      {{ chat.title }}
    </li>
  </ul>
</template>

<script setup>
import { ref } from 'vue'

const chats = ref([
  { id: 1, title: 'Chat 1' },
  { id: 2, title: 'Chat 2' },
  // Add more chats as needed
])

const selectChat = (chat) => {
  console.log('Selected chat:', chat)
  // Implement chat selection logic
}
</script>

<style scoped>
.chat-list {
  list-style-type: none;
  padding: 0;
}

.chat-list li {
  padding: 0.5rem;
  cursor: pointer;
}

.chat-list li:hover {
  background-color: #e0e0e0;
}
</style>
