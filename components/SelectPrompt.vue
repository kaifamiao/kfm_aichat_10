<template>
  <select v-model="selectedPrompt">
    <option v-for="prompt in prompts" :key="prompt.id" :value="prompt.id">
      {{ prompt.name }}
    </option>
  </select>
</template>

<script setup>
import { ref } from 'vue'

const prompts = ref([
  { id: 1, name: 'Prompt 1' },
  { id: 2, name: 'Prompt 2' },
  { id: 3, name: 'Prompt 3' },
])

const selectedPrompt = ref(1)
</script>
