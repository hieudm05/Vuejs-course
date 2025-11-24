<script setup>
import { ref } from 'vue';

const ItemsShopping = ref([
  { id: 1, name: "Apples", quantity: 5 },
  { id: 2, name: "Bananas", quantity: 3 },
  { id: 3, name: "Oranges", quantity: 4 },
]);
</script>
<template>
  <ul>
    <li v-for="item in ItemsShopping" :key="item.id">
      {{ item.name }} - Quantity: {{ item.quantity }}
    </li>
  </ul>
  <!-- Chạy từ 1 đến 10 -->
  <span v-for="n in 10" :key="n">{{ n }}</span>
</template>
