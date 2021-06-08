<template>
  <div>
    <div :key="task.id" v-for="task in tasks">
        <Task :task="task"></Task>
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
    }
}
</script>

<style>

</style>