<script setup>
import { reactive, ref } from 'vue';

const todoText = ref('');
const todos = reactive([
  { id: 1, text: 'Learn Vue.js', done: false },
  { id: 2, text: 'Build a to-do app', done: false },
  { id: 3, text: 'Master Vue Router', done: false },
]);

const addToDo = () => {
  if(todoText.value.trim() === '') return;
  const newTodo = {
    id: todos.length + 1,
    text: todoText.value,
    done: true
  }
  todos.push(newTodo);
  todoText.value = '';
}

</script>
<template>
  <input type="text" v-model="todoText" placeholder="Add a new to-do" @keyup.enter="addToDo" />
  <button @click="addToDo">Add todo</button>
  <hr>
  <ul>
    <li v-for="item in todos" :key="item.id">
      {{ item.text }} - <strong>{{ item.done ? 'Done' : 'Not Done' }}</strong>
    </li>
  </ul>
</template>
