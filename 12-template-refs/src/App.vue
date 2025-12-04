<script setup>
import { nextTick, onMounted, ref } from 'vue';
// Khi nào cần sử dụng refs: 
// Khi mà ta muốn thao tác với DOM trực tiếp
// Muốn thao tác với các thư viện trên JS bên ngoài (jquery)
// Cần quản lý trạng thái của các phần tử
// Tối ưu hiệu suất (tìm kiếm DOM nhanh chóng)

  const list = ref(["Item1", "Item2", "Item3"]);
  const itemsList = ref([])
 onMounted(async () => {
  await nextTick();
  itemsList.value.forEach(item => {
    item.style.transition = "opacity 10s";
    // requestAnimationFrame: cho trình duyệt đợi lại 1 nhịp để chạy từng hiệu ứng
    requestAnimationFrame(() => {
      item.style.opacity = 1;
      item.style.color = "red"
    })
  });
});
</script>
<template>
  <h1>Refs với v-for</h1>
  <ul>
  <li v-for="(value, index) in list"  :key="index" ref="itemsList" style="opacity: 0"> {{ value }}</li>
  </ul>
</template>
