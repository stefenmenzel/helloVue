<template>
    <div class="todoItemDiv">
        <div class="todoItem">
            <span>{{todo}}</span>
            <input type="checkbox" v-model="completed" />
        </div>        
    </div>
</template>

<script>
    export default {
        name: "TodoItem",
        props: {
            todo: String,
            completed: Boolean
        }
    }
</script>