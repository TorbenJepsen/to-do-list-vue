<template>
  <div id="app">
    <img src="./assets/logo.png">
    <to-do-list v-bind:todos="todos"></to-do-list>
  </div>
</template>


<script>
import ToDoList from "./components/ToDoList";

export default {
  name: "app",
  components: {
    ToDoList
  },
  data() {
    return {
      todos: [
        {
          title: "To Do A",
          project: "Project A",
          done: false
        },
        {
          title: "To Do B",
          project: "Project A",
          done: false
        },
        {
          title: "To Do C",
          project: "Project C",
          done: false
        },
        {
          title: "To Do D",
          project: "Project D",
          done: false
        }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
