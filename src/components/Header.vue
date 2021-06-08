<template>
    <header>
        <h1>{{ title }}</h1>
    </header>
</template>

<script>
export default {
    name: "Header",
    
    props: {
        title: String
    }
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: lavender;
        border: 1px solid #cecedf;
    }
</style>