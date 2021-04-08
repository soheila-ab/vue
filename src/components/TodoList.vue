<template>
  <div>
    <input
      type="text"
      class="todo-input"
      placeholder="enter your name"
      v-model= "newTodo"
      @keyup.enter= "addtodo"
   />
    <div v-for= "(todo, index) in todos" :key= "todo.id" class="todo-item">
      <input type="checkbox" v-model= "todo.completed" class="checkbox" />

      <div>
        <div
          v-if= "!todo.editing"
          @dblclick= "editTodo(todo)"
          class="todo-item-label"
          :class= "{ completed: todo.completed }"
        >
          {{ todo.title }}
        </div>
      </div>
      <div class="remov-item" @click="removeTodo(index)">&times;</div>
    </div>
  </div>
</template>



<script>
export default {
  name: "TodoList",
  idfortodo: 3,
  data() {
    return {
      newTodo: "",
      todos: [
        {
          id: 1,
          title: "test1",
          completed: false,
        },
        // {
        //   id: 2,
        //   title: "test2",
        //   completed: false,
        // },
      ],
    };
  },
  methods: {
    addtodo() {
      if (this.newTodo.trim().length == 0) {
        return;
      }

      this.todos.push({
        id: this.idfortodo,
        title: this.newTodo,
        completed: false,
      });
      this.newTodo = "";
      this.idfortodo++;
    },
    removeTodo(index) {
      this.todos.splice(index, 1);
    },
  },
};
</script>

<style scoped>
.todo-input {
  width: 500px;
  padding: 10px 18px;
  font-size: 18px;
  margin-bottom: 16px;
  margin-top: 16px;
}
.todo-item {
  margin-bottom: 12px;
  /* position: absolute; */
  margin-right: 50 px;
  display: flex;
  align-items: center;
  padding: 10px 50px;
  justify-content: space-between;
}
.remove-item {
  cursor: pointer;
  margin-left: 16px;
}
.completed {
  text-decoration: line-through;
  color: blue;
  background-color: chartreuse;
}
</style>