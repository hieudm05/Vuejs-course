<script setup>
import { ref } from "vue";

const users = ref([
  {
    name: "John Doe",
    age: 30,
    isActive: true,
  },
]);
</script>
<template>
  <ul>
    <!-- Khi sử dụng cả v-if và v-for phải bọc ngoài thẻ template("thẻ này không sinh thêm element") -->
    <!-- Vì vuejs không chấp nhận đặt cả v-if và v-for trên cùng 1 thẻ html -->
    <template v-for="(user, index) in users" :key="user.name">
      <li v-if="user.isActive">{{ user.name }} ({{ index }})</li>
    </template>
  </ul>

  <!-- Tại sao sử dụng key -->
  <!-- Key là duy nhất trong v-for giúp cho DOM theo dõi sự thay đổi của các phần tử   -->
  <!-- Tối ưu hoá DOM -->
  <!-- Quản lí hiệu xuất -->
  <!-- Nếu không có key thì Vuejs sẽ sử dụng thuật toán tương đối để cập nhật phần tử,.... -->
  

</template>
