<template>
    <div>
        <input type="text" name="task" id="task" @keyup.enter="buildTask" v-model="text" placeholder="The name of the task goes here">
        <Button @add-task="buildTask" text="Add Task" color="#75b999"></Button>
    </div>
</template>

<script>

import Button from "./Button";
const dayjs = require('dayjs');


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
         * Builds a new task object with text that is the same as the input field and the current date parsed with day.js
         */
        buildTask() {
            const currentDay = dayjs().format("DD/MM/YY");
            const currentHour = dayjs().format("hh:mm");

            const newTask = {
                text: this.text,
                date: `${currentDay} at ${currentHour}`,
                id: ""
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
        background-color: #301d6eab;
        border: 1px solid pink;
    }

    input {
        padding: 5px 10px;
        margin-right: 20px;
    }
</style>