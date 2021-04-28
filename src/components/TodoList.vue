<template>
  <div>
  <h1>Todo application</h1>
  <hr/>
    <ul>
      <TodoItem
       v-for="todo of todos"
       :key="todo.id"
       v-bind:todo="todo"
       />
    </ul>
  </div>
</template>

<script>
import TodoItem from './TodoItem'

export default {
  props: ['todos'],
  components: {
    TodoItem
    }
}
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>