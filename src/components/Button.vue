<template>
    <button @click="$emit('add-task')" :style="{ background: color }">{{ text }}</button>
</template>

<script>
export default {
    name: "Button",
    
    props: {
        text: String,
        color: String
    }
}
</script>

<style scoped>
    button {
        display: inline-block;
        color: #fff;
        font-weight: bold;
        border-top: 0;
        border-left: 0;
        border-bottom: 2px solid rgb(93, 93, 93);
        border-right: 2px solid rgb(93, 93, 93);
        padding: 10px 20px;
        margin: 5px;
        border-radius: 5px;
        cursor: pointer;
        text-decoration: none;
        font-size: 15px;
        font-family: inherit;
        transition: 0.2s;
    }
    button:hover {
        box-shadow: 4px 4px 10px rgb(46 46 46);
    }
    button:focus {
        outline: none;
    }
    button:active {
        transform: scale(0.90);
    }
</style>