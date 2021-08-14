<template>
    <div class="task">
        <h2>{{ task.text }}</h2>
        <div>Added on {{ task.date }}</div>
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
    .task {
        background-color: #c8bee2;
        border: 1px solid #cecedf;
        padding: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .task > * {
        flex: 1;
    }

    h2 {
        margin: 0;
        overflow: hidden;
        text-overflow: ellipsis;
    }

    i {
        font-size: 30px;
        color: red;
        cursor: pointer;
    }
</style>