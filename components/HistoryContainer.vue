<template>
  <div class="history-container">
    <ChatList />
  </div>
</template>

<script setup>
import ChatList from './ChatList.vue'
</script>

<style scoped>
.history-container {
  height: calc(100vh - 200px);
  overflow-y: auto;
}
</style>
