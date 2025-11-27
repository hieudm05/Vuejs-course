<script setup>
import { ref } from 'vue';

const count = ref(0);
const greet = (event) => {
  console.log(event.target);
  alert(`Hello! Event type: ${event.type}`);
}
const sayHi = (name) => {
  alert(`Hi ${name}`);
}

</script>
<template>
  <h2>Event handling</h2>
  <p>Count: {{ count }}</p>
  <button @click="count++">Tăng</button>
  <button @click="greet">event</button>
  <button @click="sayHi('Vue Learner')">Say Hi</button>
</template>
