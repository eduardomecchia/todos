<template>
    <button @click="onClick()" :style="{ background: color }">{{ text }}</button>
</template>

<script>
export default {
    name: "Button",
    
    props: {
        text: String,
        color: String
    },

    methods: {
        onClick() {
            console.log("Click");
        }
    }
}
</script>

<style scoped>
    button {
        display: inline-block;
        background: #000;
        color: #fff;
        border: none;
        padding: 10px 20px;
        margin: 5px;
        border-radius: 5px;
        cursor: pointer;
        text-decoration: none;
        font-size: 15px;
        font-family: inherit;
    }
    button:focus {
        outline: none;
    }
    button:active {
        transform: scale(0.98);
    }
</style>