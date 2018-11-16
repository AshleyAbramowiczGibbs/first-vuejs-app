<template>
  <div class="home">
    <h1>Add a to do item</h1>
    <button v-on:click="addToDo()">Add To Do Item!</button>
    <h1>{{ message }}</h1>
    <div v-for="todos in todo">
      <p>{{ todos.text }} </p>
    </div>
  </div>
</template>


<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      todo: [
        {
          id: 1,
          text: "Thank you notes",
          complete: false
        },
        {
          id: 2,
          text: "Run",
          complete: false
        },
        {
          id: 3,
          text: "Read my book",
          complete: false
        }
      ]
    };
  },
  created: function() {
    
  },
  methods: {
    addToDo: function() {
      let newTask = {
        id: 4,
        text: "Work on capstone",
        complete: false
      };
      this.todo.push(newTask);
    }
  },
  computed: {}
};
</script>
