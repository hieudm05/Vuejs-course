<script setup>
import { reactive, ref } from 'vue';
const   borderRadius = ref(10);
const objectColor =reactive({
  border: 'none',
  padding: '10px 20px',
  backgroundColor: 'black',
  color: 'white'
})

</script>
<template>
  <button :style="[objectColor,{borderRadius: borderRadius + 'px'}]">Tìm kiếm</button>
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
