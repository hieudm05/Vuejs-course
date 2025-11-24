<script setup>
import { ref } from 'vue';

const isLoginedIn = ref(false)
const showHide = ref(false);
const changeStatus = () => {
  isLoginedIn.value = !isLoginedIn.value;
}
const showHidden = () => {
  showHide.value = !showHide.value;
}
</script>
<template>
  <p v-if="isLoginedIn">Chào mừng bạn đến trang hệ thống.</p>
  <p v-else>Vui lòng đăng nhập để tiếp tục.</p>
  <button @click="changeStatus">Change status</button>
  <hr />
  <h2>Test show hide</h2>
  <!-- v-show: nhằm mục đích ẩn hiện phần tử bằng cách thêm style thuộc tính  display: none (nếu ẩn) -->
  <p v-show="showHide">{{ showHide ? "Đã hiện" : "Đã ẩn" }}</p>
  <button @click="showHidden">Show hiden</button>
</template>

