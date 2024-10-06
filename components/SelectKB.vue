<template>
  <select v-model="selectedKB">
    <option v-for="kb in knowledgeBases" :key="kb.id" :value="kb.id">
      {{ kb.name }}
    </option>
  </select>
</template>

<script setup>
import { ref } from 'vue'

const knowledgeBases = ref([
  { id: 1, name: 'KB 1' },
  { id: 2, name: 'KB 2' },
  { id: 3, name: 'KB 3' },
])

const selectedKB = ref(1)
</script>
