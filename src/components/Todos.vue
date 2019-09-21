<template>
    <div class="list">
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
    name: "Todos",
    components: {
        TodoItem
    },
    props:["todos"]
}
</script>

<style scoped>

    .list{
        margin-left: 20%;
        margin-right: 20%;
        margin-top: 10%;
        border: 5px outset;
    }

</style>

