<template>
    <div>
    <label for="email">Email</label>
    <input type="text" v-model="email">
    <button @click="setEmailDefault">Reset</button>
    <p>{{ email }}</p>
    </div>

     <div>
    <label for="username">Username</label>
    <input type="text" v-model="username">
    <button @click="setUsernameDefault">Reset</button>
    <p>{{ username }}</p>
    </div>
</template>
<script setup>
    const email = defineModel("email")
    const [username, modifiners] = defineModel("username",{
       set(value){
        if(modifiners.capitalize){
            return value.charAt(0).toUpperCase() + value.slice(1)
        }
        return value
       }
    })
    console.log(modifiners);
    
    const setEmailDefault = () => {
        email.value = "hieudubai.@gmail.com"
    }
    const setUsernameDefault = () => {
        username.value = "hieudm"
    }
</script>