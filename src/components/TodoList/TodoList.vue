<template>
    <div class="todoDiv">
        <h2>Todo List</h2>
        <!-- <p>{{list}}</!-->
        <div class="todoList">
            <div>
                <ul>
                    <li v-for="item in list" :key="item.todo">
                        <TodoListItem v-bind:todo="item.todo" v-bind:completed="item.completed"/>   
                    </li>
                </ul>                
            </div>
        </div>
    </div>
</template>

<script>
    import TodoListItem from '../TodoListItem/TodoListItem.vue';

    export default {
        name: "TodoList",
        components: {
            TodoListItem,
        },
        props: {
            list: Array
        },
        // mounted () { 
        //  console.log("I'm running at mount") // {x:1}
        //  console.log("I'm running at mount again") // {x:1}
        // }
    }
</script>