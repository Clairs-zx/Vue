<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @toggle-add-task="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'pink' : 'skyblue'"/>
        <!-- <Button text="Update Task" color="green"/>
        <Button text="Delete Task" color="red"/> -->

    </header>
</template>

<script>
import Button from "./Button"
export default {
    name: 'Header',
    components:{
        Button
    },
    props: {
        title: {
            type: String,
            default: 'Hello World'
        },
        showAddTask: Boolean,
    },
    emits:['toggle-add-task'],
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>