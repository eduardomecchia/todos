<template>
  <div class="tasks">
    <div class="task-container" :key="task.id" v-for="task in tasks">
        <Task @delete-task="$emit('delete-task', task.id)" :task="task"></Task>
    </div>
  </div>
</template>

<script>
import Task from "./Task";

export default {
    name: "Tasks",

    components: {
        Task
    },

    props: {
        tasks: Array
    },

    emits: ["delete-task"]
}
</script>

<style scoped>
  .tasks {
    overflow-y: scroll;
    height: 75%;
    background-color: #d4d4f6;
  }
</style>