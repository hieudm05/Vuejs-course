<script setup>
import { onMounted, onUnmounted, ref } from 'vue';

const time = ref(0);
let intervalId = null
onMounted(() => {
 intervalId = setInterval(() => {
  time.value++
 },1000)
});
// Khi thoát khỏi trang này nó sẽ chạy hàm Unmounted
onUnmounted(() => {
  clearInterval(intervalId)
})
</script>
<template>
  <div class="about">
    <h1>This is an about page</h1>
    {{ time }}
  </div>
</template>

