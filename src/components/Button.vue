<template>
    <button :style="{ background: color }">{{ text }}</button>
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
        padding: 5px 25px;
        border-radius: 5px;
        background-color: color;
    }

    button:focus-visible {
        outline: 0;
    }
</style>