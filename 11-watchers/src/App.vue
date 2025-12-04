<script setup>
import { reactive, watch } from 'vue';

const user = reactive({
  age: 18,
  class:{
    student: 0,
    name: "A"
  }
})

const changeAge = () => {
  user.class.student++;
}

// Mặc định deep:true nó sẽ theo dõi sâu vào obj,
// Trường hợp deep:false nó chỉ theo dõi được tầng đầu tiên thôi
// watch(user, (newUser) => {
//   console.log("data", JSON.stringify(newUser));
  
// },{deep: true})

// immediate: chạy khi bắt đầu load vào trang, và chạy khi thay đổi data
watch(user, (newUser) => {
  console.log("data", JSON.stringify(newUser));
  
},{immediate: true})
</script>
<template>
<button @click="changeAge">Change</button>
</template>
