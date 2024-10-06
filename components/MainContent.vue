<template>
  <div class="main-content">
    <component :is="currentComponent" />
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import Chat from './Chat.vue'
import HistoryChat from './HistoryChat.vue'

const currentChatType = ref('new') // 'new' or 'history'

const currentComponent = computed(() => {
  return currentChatType.value === 'new' ? Chat : HistoryChat
})
</script>

<style scoped>
.main-content {
  flex: 1;
  overflow-y: auto;
  padding: 1rem;
}
</style>
