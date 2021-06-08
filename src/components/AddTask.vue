<template>
    <div>
        <input type="text" name="task" id="task" v-model="text" placeholder="The name of the task goes here">
        <Button @add-task="buildTask" text="Add Task" color="purple"></Button>
    </div>
</template>

<script>

import Button from "./Button";

export default {
    name: "AddTask",

    components: {
        Button
    },

    data() {
        return {
            text: ""
        }
    },

    methods: {
        /**
         * Builds a new task object with text that is the same as the input field
         */
        buildTask() {
            const newTask = {
                text: this.text,
                day: "05/12/12 at 00:00",
                id: Math.floor(Math.random() * 10000)
            }

            this.$emit("add-task", newTask);

            // Clean input field after creating new task
            this.text = "";
        }
    }
}
</script>

<style scoped>
    div {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 10px;
        background-color: lavenderblush;
    }

    input {
        padding: 5px 10px;
        margin-right: 20px;
    }
</style>