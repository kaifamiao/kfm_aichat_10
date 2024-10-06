<template>
  <select v-model="selectedOption">
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</template>

<script setup>
import { ref } from 'vue'

const selectedOption = ref('1')
</script>
