<template>
  <div id="app">
    <Header title="Eduardo's Task Tracker!" color="white" background="red"></Header>
    <AddTask></AddTask>
    <Tasks :tasks="tasks"></Tasks>
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
          {
            text: "Code",
            id: 0,
            date: "08/06/21 at 15:00"
          },
          {
            text: "Eat",
            id: 1,
            date: "08/06/21 at 17:00"
          },
          {
            text: "Sleep",
            id: 2,
            date: "08/06/21 at 19:00"
          }
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
