<script setup>
const emit= defineEmits(['increase','increaseByTwoTimes','increaseBy'])
const callFunctionIncrease = () => {
    emit("increase")
}
const callFunctionIncreaseByTwoTimes = () => {
    emit('increaseByTwoTimes')
}
const callFunctionIncreaseBy = () => {
    emit("increaseBy",5, 20)
}
</script>
<template>
    <button @click="callFunctionIncrease">Increase</button>
    <button @click="callFunctionIncreaseByTwoTimes">Increase By Two Times</button>
    <button @click="callFunctionIncreaseBy">Increase By</button>
</template>