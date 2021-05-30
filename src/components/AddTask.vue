<template>
    <div>
        <input type="text" name="task" id="task">
        <Button text="Add" color="green"></Button>
    </div>
</template>

<script>
import Button from "./Button"

export default {
    name: "AddTask",
    components: {
        Button
    }
}
</script>

<style scoped>
    div {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    input {
        padding: 5px 10px;
        margin-right: 20px;
    }
</style>