<template>
  <div>
      <p>Completed Tasks: {{todos.filter(todo => {return todo.done === true}).length}}</p>
      <p>Pending Tasks: {{todos.filter(todo => {return todo.done === false}).length}}</p>
        <to-do v-for="todo in todos" v-bind:todo="todo" v-bind:key="todo.title"></to-do>
  </div>
</template>

<script type = "text/javascript">

import ToDo from './ToDo';

export default {
  props: ["todos"],
  components: {
      ToDo,
  }
};
</script>

<style>
</style>