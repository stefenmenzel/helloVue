<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="We done made a helloworld of a vue app"/>
    <TodoList v-bind:list="list" @toggled="toggleItem"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TodoList from './components/TodoList/TodoList.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    TodoList
  },
  data() {
    return{
      list:[
        {
          todo: "poop",
          completed: true,
        },
        {
          todo: "learn vue",
          completed: false,
        }
      ]
    }    
  },
  methods: {
    toggleItem(index) {
      console.log('this.list', this.list);
      this.list[index].completed = !this.list[index].completed
      // console.log('toggled', index);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
