<template>
<div class="app ">
  <Cabecalho nome="Todo List"/>  
  <MainTodo/>
</div>  
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Cabecalho from './components/Cabecalho.vue'
import MainTodo from './components/MainTodo.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Cabecalho,
    MainTodo
  }  
}
</script>

<style>
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
  /* background-color: aquamarine; */
  background-color: white;
}

</style>
