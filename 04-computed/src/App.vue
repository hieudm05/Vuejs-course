<script setup>
import { computed, reactive } from 'vue';

  const books = reactive({
    name: 'book1',
    chapters: []
  })
  // computed:
  // Tính hiểu quả
  // + Nó sẽ tính toán logic 1 phần data trong 1 object cần xử lí
  // + Nó chỉ tính toán lại nếu các phụ thuộc nó thay đổi thôi 
  // Tính phản ứng (reactivity): giúp cập nhật state và giao diện mượt mà và kịp thời
  // Tính tài sử dụng code

  const idPublic = computed(() => books.chapters.length ? "Có":"Không")
  
</script>
<template>
  <p>Tên sách: {{ books.name }}</p>
  <p>Xuất bản: {{ idPublic }}</p>
</template>
