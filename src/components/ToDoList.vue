<template>
  <div>
      <p>Completed Tasks: {{todos.filter(todo => {return todo.done === true}).length}}</p>
      <p>Pending Tasks: {{todos.filter(todo => {return todo.done === false}).length}}</p>
      <to-do v-on:delete-todo="deleteTodo" v-on:complete-to-do="completeToDo"
       v-for="todo in todos" :todo.sync="todo" v-bind:key="todo.title">
      </to-do>
  </div>
</template>

<script type = "text/javascript">

import ToDo from './ToDo';

export default {
  props: ['todos'],
  components: {
    ToDo,
  },
  methods: {
    deleteTodo(todo) {
      const todoIndex = this.todos.indexOf(todo);
      this.todos.splice(todoIndex, 1);
    },
    completeToDo(todo) {
      const todoIndex = this.todos.indexOf(todo);
      this.todos[todoIndex].done = true;
    },
  },
};
</script>

<style>
</style>
