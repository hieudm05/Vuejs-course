<script setup>
import { computed, reactive, ref } from "vue";

const fisrtName = ref("Nguyễn Văn");
const lastName = ref("A");
const fullName = computed({
  get() {
    return fisrtName.value + " " + lastName.value;
  },
  set(newVal) {
    [fisrtName.value, lastName.value] = newVal.split(",")
  },
});
// writable: ghi đè trong computed
// Vì trong computed chỉ xử lí đọc dữ liệu, nên là nếu để thêm data hoặc thay đổi data thì phải xử dụng getter and setter
const changeFullname = () => {
  return fullName.value = "Đoàn Di,Băng"
}
</script>
<template>
  <h1>Writable</h1>
  <p>Full Name {{ fullName }}</p>
  <button @click="changeFullname">Thay đổi</button>
</template>
