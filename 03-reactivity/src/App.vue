<script setup>
import { reactive, ref } from "vue";
// const count = ref(0);

// const object = ref({
//   count: 1,
//   user: {
//     age: 18,
//   },
//   array: [1, 2, 3],
// });
// const change = () => {
//   object.value.count++
// };

// Nếu với mảng hay object nên dùng reactive thì không cần .value nữa

const object = reactive({
  count: 1,
  user: {
    age: 18,
  },
  array: [1, 2, 3],
});
const change = () => {
  object.count++
};
// const increase = () => count.value++;
</script>
<template>
  <!-- Reactivity (Tính phản ứng) -->
  <div>{{ object.count }}</div>
  <button @click="change">Increase</button>
</template>
