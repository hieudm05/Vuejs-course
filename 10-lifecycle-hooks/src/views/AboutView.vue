<script setup>
import { onMounted, onUnmounted, ref, onBeforeMount, onBeforeUnmount } from 'vue';

const time = ref(0);
let intervalId = null

onBeforeMount(() => {
  console.log('on before mount');
})
onMounted(() => {
  console.log("on mounted");
  
 intervalId = setInterval(() => {
  time.value++
 },1000)
});

onBeforeUnmount(() => {
  console.log('on before unmount');
})
// Khi thoát khỏi trang này nó sẽ chạy hàm Unmounted
onUnmounted(() => {
  console.log("on Unmoutedf");
  
  clearInterval(intervalId)
})
</script>
<template>
  <div class="about">
    <h1>This is an about page</h1>
    {{ time }}
  </div>
</template>

