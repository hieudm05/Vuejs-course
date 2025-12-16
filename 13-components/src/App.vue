<script setup>
import { ref, watchEffect } from "vue";
import ButtonCount from "./components/ButtonCount.vue";
import HelloWorld from "./components/HelloWorld.vue";
import ComponentVmodel from "./components/ComponentVmodel.vue";
const stringNew = ref("đã thêm");
const count = ref(0);
const increaseBy = (number1, number2) => {
  count.value = count.value + number1 + number2
}
const email = ref("")
const username = ref("")
watchEffect(() => {
  console.log(email.value);
})

</script>

<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <!-- <hello-world :greeting-message="count" /> -->
  <!-- <button-count @increase="count++" @increaseByTwoTimes="count+=2" @increaseBy="increaseBy" /> -->
  <component-vmodel v-model:email="email" v-model:username="username"/>
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
