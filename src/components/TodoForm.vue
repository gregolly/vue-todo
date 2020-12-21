<template>
  <div>
    <input type="text" v-model="newTodoItem"/>
    <button @click="addNewTodoItem" type="submit">submit</button>
  </div>
</template>

<script>
export default {
  data(){
    return{
      newTodoItem: ""
    }
  },
  methods:{
    addNewTodoItem(){
      this.$store.dispatch('addNewTodo',this.newTodoItem)
      this.newTodoItem = ''
    }
  }
}
</script>

<style>
input{
    width: 300px;
    padding: 5px 10px;
    border: none;
}
button[type=submit]{
  background: none;
    color: #fff;
    border: none;
    background-color: #ccc;
    padding: 5px;
    cursor: pointer;
}
</style>