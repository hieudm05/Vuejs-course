<template>
    <div>
    <label for="email">Email</label>
    <input type="text" v-model="email">
    <button @click="setEmailDefault">Reset</button>
    <p>{{ email }}</p>
    </div>
</template>
<script setup>
    const email = defineModel()
    const setEmailDefault = () => {
        email.value = "hieudubai.@gmail.com"
    }
</script>