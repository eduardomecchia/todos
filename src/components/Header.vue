<template>
    <header :style="{ background: background }">
        <h1 :style="{ color: color }">{{ title }}</h1>
    </header>
</template>

<script>
export default {
    name: "Header",
    
    props: {
        title: String,
        color: String,
        background: String
    }
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: lightblue;
    }
</style>