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

</style>