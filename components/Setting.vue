<template>
  <div class="setting">
    <button @click="openSettingsModal">Settings</button>
  </div>
</template>

<script setup>
const openSettingsModal = () => {
  // Implement logic to open settings modal
  console.log('Opening settings modal')
}
</script>

<style scoped>
.setting {
  padding: 1rem;
}
</style>
