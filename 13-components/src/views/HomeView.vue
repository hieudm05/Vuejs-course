<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>Trang home view: {{local}}</p>
  </div>
</template>
<script setup>
  import { inject } from 'vue';
const {local} = inject('local')
</script>
