<template>
    <div>
        <h1>TODO LIST</h1>
        <Todo v-for="todo of todos" :key="todo.id" :todo="todo"/>
    </div>
</template>
<script>
import Todo from "../components/ToDoComponent.vue"
    export default {
        components: {
            Todo
        },
        
        data() {
            return {
                todos: []
            }

        },
        async mounted() {
            let result = await fetch('https://jsonplaceholder.typicode.com/todos');
            let todos = await result.json();

            this.todos = todos;
        },
        
        method() {
            
        }
    }

</script>