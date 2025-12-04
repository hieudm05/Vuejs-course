<script setup>
import { onMounted, ref } from 'vue';

const inputRef = ref(null)
onMounted(() => {
  inputRef.value.focus()
})
</script>
<template>
  <h1>Template refs</h1>
  <input type="text" ref="inputRef">
<button @click="changeAge">Change</button>
</template>
