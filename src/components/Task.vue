<template>
    <div>
        <h2>{{ task.text }}</h2>
        <span>Added on {{ task.date }}</span>
        <i @click="$emit('delete-task', task.id)" class="fas fa-times"></i>
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
        background-color: #9c90c086;
        border: 1px solid #cecedf;
        padding: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    h2 {
        margin: 0;
    }

    i {
        font-size: 30px;
        color: red;
        cursor: pointer;
    }
</style>