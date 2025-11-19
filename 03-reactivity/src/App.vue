
<script setup>
import { ref } from 'vue';
const count = ref(0)
const increase = () => count.value++
</script>
<template>
  <!-- Reactivity (Tính phản ứng) -->
  <div>{{ count }}</div>
  <button @click="increase">Increase</button>
</template>