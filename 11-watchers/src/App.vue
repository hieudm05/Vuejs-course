<script setup>
import { ref, watch } from 'vue';

const x = ref(0);
const y = ref(0);
// Lưu í: wactch nó không theo dỗi được sự thay đổi của thuộc tính nhé,
// Ví dụ như tuổi trong 1 reactive khi tăng nó không theo dỗi được, 
// Nhưng nếu muốn theo dõi thì sử dụng getter () =>
const Increment = () => {
  x.value = Math.floor(Math.random() * 11);
  y.value = Math.floor(Math.random() * x.value)
}
// watch(() => x.value + y.value, (sum) => {
//   console.log(`Tổng ${sum}`);
  
// })
watch([x, () => y.value+ 1], ([newX, newY]) => {
  console.log(`New x ${newX} và New Y ${newY}`);
})
</script>
<template>
<p>{{ x }}, {{ y }}</p>
<button @click="Increment">Increment</button>
</template>
