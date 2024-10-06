<template>
  <select v-model="selectedModel">
    <option v-for="model in models" :key="model.id" :value="model.id">
      {{ model.name }}
    </option>
  </select>
</template>

<script setup>
import { ref } from 'vue'

const models = ref([
  { id: 1, name: 'Model 1' },
  { id: 2, name: 'Model 2' },
  { id: 3, name: 'Model 3' },
])

const selectedModel = ref(1)
</script>
