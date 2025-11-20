<script setup>
import { computed, ref } from "vue";

const isActive = ref(true);
const hasError = ref(false);

const isStatus = computed(() => ({
  active: isActive.value && !hasError.value,
  "has-error": hasError.value,
}));
const changeActive = () => {
  isActive.value = !isActive.value;
};
</script>
<template>
  <!-- Lý do 'has-error' phải để trong dấu nháy vì nó có ký tự đặc biệt là "-" -->
  <button @click="changeActive" class="btn" :class="isStatus">Nút</button>
</template>
<style>
.btn {
  background-color: peru;
  border-radius: 10px;
  padding: 10px 20px;
  border: none;
}
.active {
  background-color: blue;
  color: white;
}
.has-error {
  background-color: red;
  color: white;
}
</style>
