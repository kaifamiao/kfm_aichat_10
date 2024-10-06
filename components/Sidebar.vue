<template>
  <aside :class="{ 'sidebar': true, 'sidebar-hidden': !isVisible }">
    <NewChat />
    <HistoryContainer />
    <Setting />
  </aside>
</template>

<script setup>
import { ref } from 'vue'
import NewChat from './NewChat.vue'
import HistoryContainer from './HistoryContainer.vue'
import Setting from './Setting.vue'

const isVisible = ref(true)

const toggleSidebar = () => {
  isVisible.value = !isVisible.value
}

defineExpose({ toggleSidebar })
</script>

<style scoped>
.sidebar {
  width: 250px;
  background-color: #f8f8f8;
  transition: width 0.3s;
}

.sidebar-hidden {
  width: 0;
  overflow: hidden;
}
</style>
