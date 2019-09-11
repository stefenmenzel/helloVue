<template>
    <div class="todoItemDiv">
        <div class="todoItem">
            <span>{{todo}}</span>
            <input type="checkbox" v-model="completed" @change="toggle"/>
        </div>        
    </div>
</template>

<script>
    export default {
        name: "TodoItem",
        props: {
            todo: String,
            completed: Boolean,
            keyIndex: Number,
        },
        methods: {
            toggle(){
                // this.$emit('toggled', this.$vnode.key);
                this.$emit('toggled', this.keyIndex);
            },
        }        
    }
</script>