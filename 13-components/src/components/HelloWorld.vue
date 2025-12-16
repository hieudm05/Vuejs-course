<script setup>
  const props = defineProps({
    // Nên khai báo tên props theo kiểu camelCase
    greetingMessage: String
  });
  console.log(props);
  // Sử dụng props như là 1 giá trị mặc định
</script>
<template>
  <div class="hello">
    <h1>{{ greetingMessage }}</h1>
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
