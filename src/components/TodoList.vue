<template>
  <div>
    <Todo v-for="(todo,index) in todos" :key="index" :todo="todo"/>
  </div>
</template>

<script>
import {mapState} from 'vuex'
import Todo from './Todo'
export default {
  components:{
    Todo
  },
  computed:{
    ...mapState({
      todos: "todos"
    })
  }
}
</script>

<style scoped>
div{
  margin-bottom: 10px;
}
</style>