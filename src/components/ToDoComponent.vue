<template>
    <div>
        <div class='titre'>
            {{todo.title}}
       </div>
       <div v-if="todo.completed" class='ok'>Terminé ! </div>
       <div v-else class="nok">A faire</div>
    </div>
</template>
<script>

    export default {
        
        name: "ToDo",
        props: {
            todo: Object
        },
        
        data() {

            return {

            }
        },
        
        methods: {
            
        },
    }
</script>

<style>
.ok {
    color:rgb(7, 255, 7);
}
.nok {
    color:red;
}
</style>