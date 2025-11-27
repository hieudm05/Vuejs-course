<script setup>
const message = () => {
  alert('Form submitted!');
}
</script>
<template>
  <h2>Key modifier</h2>
  <input @keyup.enter="message" type="text" placeholder="Press Enter to submit" />
  <button type="submit">Submit</button>
</template>
