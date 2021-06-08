<template>
    <footer>
        <div>
            <span>This app was made using 
                <a href="https://vuejs.org/" target="_blank">Vue.js</a> 
                2 and 
                <a href="https://cli.vuejs.org/" target="_blank">Vue CLI</a> 
                , with the help of Brad Traversy's amazing
            </span>

            <a href="https://www.youtube.com/watch?v=qZXt1Aom3Cs" target="_blank">Vue.js Crash Course 2021.</a>
            </div>
    </footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped>
    footer {
        background-color: #301d6eab;
        border: 1px solid pink;
        padding: 30px;
        color: white;
    }

    div {
        font-size: 13px;
    }
</style>