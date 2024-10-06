<template>
  <main class="main">
    <MainHeader @toggle-sidebar="toggleSidebar" />
    <MainContent />
    <ChatInput />
  </main>
</template>

<script setup>
import { ref } from 'vue'
import MainHeader from './MainHeader.vue'
import MainContent from './MainContent.vue'
import ChatInput from './ChatInput.vue'

const emit = defineEmits(['toggle-sidebar'])

const toggleSidebar = () => {
  emit('toggle-sidebar')
}
</script>

<style scoped>
.main {
  flex: 1;
  display: flex;
  flex-direction: column;
}
</style>
