<script setup>
import { inject, ref } from 'vue';
const injected = inject('local',{
  local: ref('JAV'),
  updateLocal: () => {}
})
const {local, updateLocal} = injected
  const props = defineProps({
    // Nên khai báo tên props theo kiểu camelCase
    greetingMessage: Number
  });
  
  // console.log(props);
  // Sử dụng props như là 1 giá trị mặc định
</script>
<template>
  <div class="hello">
    <h1>{{ greetingMessage }}</h1>
    <p>Trang hello: {{local}}</p>
    <button @click="updateLocal">Update date local</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
