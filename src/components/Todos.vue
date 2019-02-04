<template>
  <div>
    <div v-for="todo in todos" :key="todo.id">
      <todo-item :todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"></todo-item>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "Todos",
  props: ["todos"],
  components: {
    TodoItem
  }
}
</script>

<style scoped>

</style>
