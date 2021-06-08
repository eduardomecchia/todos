<template>
  <div id="app">
    <Header title="Eduardo's Task Tracker"></Header>
    <AddTask @add-task="addTask"></AddTask>
    <Tasks @delete-task="deleteTask" :tasks="tasks"></Tasks>
    <div v-if="tasks.length === 0">Congratulations! You completed all of your tasks.</div>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header";
import AddTask from "./components/AddTask";
import Tasks from "./components/Tasks";
import Footer from "./components/Footer";

export default {
  name: 'App',

  components: {
    Header,
    AddTask,
    Tasks,
    Footer
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
    },

    /**
     * Add a new task to the app
     * @param {object} task - The task object that is built in AddTask component
     */
    addTask(task) {
      // Validate task creation, rejecting empty names
      if (!task.text) {
        alert("The task you're trying to create has an empty name");
        return
      }

      this.tasks.push(task);
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
}

a {
  color: #c3e4d6;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
a:active, a:visited:active {
  color: red;
}
a:visited {
  color: #5094a7;
}
</style>
