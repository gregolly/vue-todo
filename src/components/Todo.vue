<template>
  <div class="todo">
    <div class="justify-content-between d-flex">
      <span :class="{completed: todo.completed}" @click="toggleTodoStatus(todo)">
        {{ todo.title }}
      </span>
      <button @click="deleteTodoItem(todo)">Delete</button>
    </div>
  </div>
</template>

<script>
import { mapActions } from 'vuex'
export default {
  props:['todo'],
  methods:{
    ...mapActions({
      deleteTodoItem: 'deleteTodoItem',
      toggleTodoStatus: 'toggleTodoStatus'
    })
  }
}
</script>

<style scoped>
.todo{
  width: 350px;
  margin: 5px auto;
}
.d-flex{
  display: flex;
}
.justify-content-between{
  justify-content: space-between;
}
.completed{
  text-decoration: line-through;
}
button{
  background: none;
    color: #fff;
    border: none;
    background-color: #84e;
    padding: 5px;
}
</style>