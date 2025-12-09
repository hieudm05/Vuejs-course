<script setup>
import { ref, onBeforeUpdate, onUpdated } from 'vue';

const count = ref(0);

const increment = () => {
  count.value++
}
onBeforeUpdate(() => {
  // console.log("on before update");
  console.log(document.getElementById('count').textContent);
})
onUpdated(() => {
  // console.log("on updated");
    console.log("onUpdated",document.getElementById('count').textContent);
})
</script>
<template>
  <div class="about">
    <h1 id="count"> {{ count }}</h1>
    <button @click="increment">increment</button>
  </div>
</template>

