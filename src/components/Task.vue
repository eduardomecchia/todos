<template>
    <div>
        <h2>{{ task.text }}</h2>
        <i class="fas fa-times"></i>
    </div>
</template>

<script>
export default {
    name: "Task",
    props: {
        task: Object
    }
}
</script>

<style scoped>
    div {
        background-color: lavender;
        border: 1px solid #cecedf;
        padding: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    h2 {
        margin: 0;
    }
</style>