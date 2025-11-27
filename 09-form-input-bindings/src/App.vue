<script setup>
import { ref } from 'vue';

const text = ref('Xin chào');
const mutilineText = ref('')
const checkNames = ref([]);
const radioChecked = ref('');
const selected = ref('');

</script>
<template>
  <h2>Form Input Bindings</h2>

  <p>Text {{ mutilineText }}</p>
   <textarea v-model="mutilineText" placeholder="Input your message" />

    <p>Checkbox {{ checkNames }}</p>
    <label >A</label>
    <input id="a" type="checkbox" v-model="checkNames" value="A" placeholder="Input your message" />

    <label for="b">B</label>
    <input id="b" type="checkbox" v-model="checkNames" value="B" placeholder="Input your message" />

     <p>Radio {{ radioChecked }}</p>
    <label for="a">A</label>
    <input id="a" type="radio" v-model="radioChecked" value="A" placeholder="Input your message" />
    
    <label for="b">B</label>
    <input id="b" type="radio" v-model="radioChecked" value="B" placeholder="Input your message" />


    <p>Select {{ selected }}</p>
    <select v-model="selected">
      <option value="" disabled>Hãy chọn đáp án</option>
      <option value="A">A</option>
      <option value="B">B</option>
      <option value="C">C</option>
    </select>
</template>
