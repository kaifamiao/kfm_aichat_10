<template>
  <footer class="footer">
    <p>&copy; {{ currentYear }} kaifamiao. All rights reserved.</p>
  </footer>
</template>

<script setup>
import { ref } from 'vue'

const currentYear = ref(new Date().getFullYear())
</script>

<style scoped>
.footer {
  text-align: center;
  padding: 1rem;
  background-color: #f0f0f0;
}
</style>
