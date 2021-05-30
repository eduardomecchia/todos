<template>
  <div id="app">
    <Header title="Task tracker"></Header>
    <AddTask></AddTask>
  </div>
</template>

<script>
import Header from "./components/Header";
import AddTask from "./components/AddTask";

export default {
  name: 'App',
  components: {
    Header,
    AddTask,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
