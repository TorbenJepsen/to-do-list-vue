<template>
  <div id="app">
    <h1 class='ui dividing centered header'>Vue.js To-Do App</h1>
    <div class='ui three column centered grid'>
    <div class='column'>
    <to-do-list v-bind:todos="todos"></to-do-list>
    <create-to-do v-on:create-to-do="createToDo"></create-to-do>
    </div>
    </div>
  </div>
</template>


<script>
import sweetalert from 'sweetalert';
import ToDoList from './components/ToDoList';
import CreateToDo from './components/CreateToDo';

export default {
  name: 'app',
  components: {
    ToDoList,
    CreateToDo,
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
  methods: {
    createToDo(newTodo) {
      this.todos.push(newTodo);
      sweetalert('Success!', 'To-Do created!', 'success');
    },
  },
};
</script>
