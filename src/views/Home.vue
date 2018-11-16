<template>
  <div class="home">
    <h1>Add a to do item</h1>
    <div>
      New Task: <input type="text" v-model="newTaskItem">
    </div>
    <button v-on:click="addToDo()">Add To Do Item!</button>
    <h1>{{ message }}</h1>
    <div v-for="todos in todo">
      <h3></h3>
      <p>{{ todos.text }} </p>
    </div>
  </div>
</template>


<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      newTaskItem: "",
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
      if (this.newTaskItem !== "") {
        let newTask = {
          id: 6,
          text: this.newTaskItem,
          complete: false
        };
        this.todo.push(newTask);
        this.newTaskItem = "";
      }
    }
    // // destroyTask: function() {
    // //   this.newTaskItem.
    // }
  },
  computed: {}
};
</script>
