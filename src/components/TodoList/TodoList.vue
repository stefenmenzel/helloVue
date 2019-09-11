<template>
    <div class="todoDiv">
        <h2>Todo List</h2>
        <!-- <p>{{list}}</!-->
        <div class="todoList">
            <div>
                <p>{{test}}</p>
                <ul>
                    <li v-for="(item, index) in list" :key="index">
                        <TodoListItem @toggled="toggled" v-bind:keyIndex="index" v-bind:todo="item.todo" v-bind:completed="item.completed"/>   
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
            list: Array,
            toggleItem: Function,
        },
        data() {
            return{
                test: 'blah'
            }
        },
        methods: {
            toggled(index){                
                this.$emit('toggled', index);
                this.test = index;
            // console.log(`you have clicked on ${index}`);
            },
        }        
        // mounted () { 
        //  console.log("I'm running at mount") // {x:1}
        //  console.log("I'm running at mount again") // {x:1}
        // }
    }
</script>