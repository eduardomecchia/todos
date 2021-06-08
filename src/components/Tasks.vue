<template>
  <div>
    <div :key="task.id" v-for="task in tasks"></div>
  </div>
</template>

<script>
export default {
    name: "Tasks",
    props: {
        tasks: Array
    }
}
</script>

<style>

</style>