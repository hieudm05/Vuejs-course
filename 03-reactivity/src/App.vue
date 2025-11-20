<script setup>
import { nextTick, ref } from "vue";

const count = ref(0);
const increase = async () => {
  count.value++
  // nextTich: dùng để cập nhật DOM xong rồi mới chạy code tiếp theo 
  // Dom trong vuejs thường gom hết sự thay đổi rồi mới thay đổi một thể
  await nextTick()
  console.log(document.getElementById('count').innerText);
  
};
</script>
<template>
  <h1>xon choa</h1>
  <p id="count">{{ count }}</p>
  <button @click="increase">Nút</button>
</template>
