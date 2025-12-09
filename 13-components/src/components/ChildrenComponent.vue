<script setup>
    const props = defineProps({
        propA: Number,
        propB: [String, Number],
        propC: {
            type: String,
            require: true
        },
        propD: {
            type: Number,
            default: 100
        },
        propE: {
            type: Object
        },
        propF: {
            type: String,
            validator(value) {
                return ["error", "success", "warning", "test"].includes(value)
            }
        },
        propG: {
            type: Function
        },
        disable: Boolean
    })
    props.propG()
</script>
<template>
    <p>{{ JSON.stringify(props) }}</p>
</template>