<script setup>
const sayHi1 = () => {
  alert(`Hi 1`);
};
const sayHi2 = () => {
  alert(`Hi 2`);
};
const handleSubmit = (event) => {
  alert('Form submission prevented!');
};
</script>
<template>
  <h2>Event handling</h2>
    <!-- Sử dụng đối số event "stop" để ngăn chặn event của phần con không bị lan ra phần cha -->
  <!-- <button @click="sayHi1">
    <button @click.stop="sayHi2">Say Hi 2</button>
    Say Hi 1
  </button> -->
  <!-- <form @submit.prevent.stop="handleSubmit">
    <button type="submit">Submit</button>
  </form> -->
  <!-- "self" nó kiểm tra xem mình ấn vào sự kiện nào -->
  <button @click="sayHi1">
    <button @click.self="sayHi2">Say Hi 2</button>
    Say Hi 1
  </button>
</template>
