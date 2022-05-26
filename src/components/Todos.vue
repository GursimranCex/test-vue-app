<template>
  <div>
    <div v-bind:key="todo.id" v-for="todo in todos">
      <h3>
        <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
      </h3>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem.vue";

export default {
  name: "MyTodos",
  props: ["todos"],
  components: {
    TodoItem,
  },
};
</script>

<style scoped></style>
