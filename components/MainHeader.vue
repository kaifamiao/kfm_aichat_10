<template>
  <div class="main-header">
    <button @click="$emit('toggle-sidebar')">Toggle Sidebar</button>
    <SelectModel />
    <SelectPrompt />
    <SelectKB />
  </div>
</template>

<script setup>
import SelectModel from './SelectModel.vue'
import SelectPrompt from './SelectPrompt.vue'
import SelectKB from './SelectKB.vue'

defineEmits(['toggle-sidebar'])
</script>

<style scoped>
.main-header {
  display: flex;
  gap: 1rem;
  padding: 1rem;
  background-color: #e0e0e0;
}
</style>
