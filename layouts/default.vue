<template>
  <div class="layout">
    <Header />
    <div class="main-content">
      <Sidebar ref="sidebarRef" />
      <Main @toggle-sidebar="toggleSidebar" />
    </div>
    <Footer />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Header from '~/components/Header.vue'
import Sidebar from '~/components/Sidebar.vue'
import Main from '~/components/Main.vue'
import Footer from '~/components/Footer.vue'

const sidebarRef = ref(null)

const toggleSidebar = () => {
  sidebarRef.value?.toggleSidebar()
}
</script>

<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main-content {
  display: flex;
  flex: 1;
}
</style>
