<script setup>
import { ref, watch } from 'vue';

const question = ref("")
const isLoading = ref(false);
const answer = ref("");

watch(question, async (newValue, oldValue) => {
  if(newValue.includes("?")) {
    isLoading.value = true;
    answer.value = "Đang suy nghĩ..."
    try {
      const res = await fetch("https://yesno.wtf/api");
      answer.value = (await res.json()).answer
    } catch (error) {
      answer.value = error
    }finally{
      isLoading.value = false
    }
  }
})
</script>
<template>
 <h1>Watchers</h1>
 <p>Hỏi một câu hỏi có thể trả lời bằng "yes" hoặc "no"</p>
 <input v-model="question" :disabled="isLoading">
 <p>{{ answer }}</p>
</template>
