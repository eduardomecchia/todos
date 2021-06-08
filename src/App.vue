<template>
  <div id="app">
    <Header title="Eduardo's Task Tracker!" color="white" background="red"></Header>
    <AddTask></AddTask>
    <Tasks></Tasks>
  </div>
</template>

<script>
import Header from "./components/Header";
import AddTask from "./components/AddTask";
import Tasks from "./components/Tasks";

export default {
  name: 'App',

  components: {
    Header,
    AddTask,
    Tasks
  },

  data() {
      return {
          tasks: []
      }
  },

  created() {
      this.tasks = [
          
      ];
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
