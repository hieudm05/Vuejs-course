<script setup>
const message = "hello world";
const raw = `<span style="color: red;">v-html</span>`;
const count = 1;
const isbuttonDisable = true
const objectAtribute = {
  id: 'container',
  class: "child",
  style: {
    color: 'blue'
  }
}
const listString = 'a,b,c,d,e,f,j';
const convertToId = (data) => data.split(",").reverse().join("-")
</script>

<template>
  <h1>Syntax</h1>
  <p>{{ message }}</p>
  <p v-html="raw"></p>
  <p>{{ count }}</p>
  <!-- bind -->
  <button :id="count" :disabled="isbuttonDisable">Bấm</button>
  <!-- Ràng buộc nhiều thuộc tính động -->
  <span v-bind="objectAtribute">Ràng buộc động</span>
  <p>List string: {{ convertToId(listString)}}</p>
</template>
