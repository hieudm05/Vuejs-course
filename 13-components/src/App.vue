<script setup>
import { ref } from "vue";
import ButtonCount from "./components/ButtonCount.vue";
import HelloWorld from "./components/HelloWorld.vue";
import ChildrenComponent from "./components/ChildrenComponent.vue";
const stringNew = ref("đã thêm");
const sayHi = () => console.log("Say hi");

</script>

<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <!-- <hello-world greetingMessage="Xin lỗi mẹ mày"/> -->
  <!-- Hoặc -->
  <hello-world :greeting-message="stringNew" />
  <!-- Khi mà sử dụng binding thì nó sẽ truyền đúng biểu thức xuống là number chứ không phải String nữa -->
  <button-count :init="2" />
  <children-component
    :prop-a="1"
    :prop-d="123"
    :prop-e="{
      message: 'Thông báo',
    }"
    :prop-f="test"
    :prop-g="sayHi"
    :disable="true"
  />
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
