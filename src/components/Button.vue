<template>
    <button @click="addTask()" :style="{ background: color }">{{ text }}</button>
</template>

<script>
export default {
    name: "Button",
    
    props: {
        text: String,
        color: String
    },

    methods: {
        addTask() {
            console.log("Click");
        }
    }
}
</script>

<style scoped>
    button {
        padding: 5px 25px;
        border-radius: 5px;
        background-color: color;
    }

    button:focus-visible {
        outline: 0;
    }
</style>