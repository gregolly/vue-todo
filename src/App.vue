<template>
  <div id="app">
    <h1>Todos</h1>
    <h3>Completed: {{ completedTodos }}</h3>
    <h3>Pending: {{ pendingTodos }}</h3>
    <TodoList/>
    <TodoForm/>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import TodoList from './components/TodoList'
import TodoForm from './components/TodoForm'

export default {
  name: 'App',
  components:{
    TodoList,
    TodoForm
  },
  computed:{
    ...mapGetters({
      completedTodos: 'completedTodos',
      pendingTodos: 'pendingTodos'
    })
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
#app{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: 'roboto', sans-serif;
  background: #313131;
  padding: 30px 0;
  color: #fff;
}
</style>
