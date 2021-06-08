<template>
    <div>
        <input type="text" name="task" id="task" @keyup.enter="buildTask" v-model="text" placeholder="The name of the task goes here">
        <Button @add-task="buildTask" text="Add Task" color="#75b999"></Button>
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