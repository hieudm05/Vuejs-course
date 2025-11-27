<script setup>
import { ref } from 'vue';

const text = ref('Xin chào');

</script>
<template>
  <h2>Form Input Bindings</h2>
  <p>{{ text }}</p>
   <input v-model="text" />
</template>
