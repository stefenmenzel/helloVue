<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="We done made a helloworld of a vue app"/>
    <TodoList v-bind:list="list"/>
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
