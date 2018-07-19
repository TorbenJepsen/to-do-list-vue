<template>
  <div id="app">
    <to-do-list v-bind:todos="todos"></to-do-list>
  </div>
</template>


<script>
import ToDoList from './components/ToDoList';

export default {
  name: 'app',
  components: {
    ToDoList,
  },
  data() {
    return {
      todos: [
        {
          title: 'To Do A',
          project: 'Project A',
          done: false,
        },
        {
          title: 'To Do B',
          project: 'Project A',
          done: false,
        },
        {
          title: 'To Do C',
          project: 'Project C',
          done: false,
        },
        {
          title: 'To Do D',
          project: 'Project D',
          done: false,
        },
      ],
    };
  },
};
</script>

<style>
</style>
