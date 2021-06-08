<template>
  <div id="app">
    <Header title="Eduardo's Task Tracker"></Header>
    <AddTask></AddTask>
    <Tasks @delete-task="deleteTask" :tasks="tasks"></Tasks>
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

  methods: {
    /**
     * Filter the tasks array, returning everything BUT the task that the user wants to delete
     * @param {string} id - ID pointing to desired task
     */
    deleteTask(id) {
      if (confirm("Are you sure you want to delete this task?")) {
        this.tasks = this.tasks.filter(task => task.id !== id);
      }
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
