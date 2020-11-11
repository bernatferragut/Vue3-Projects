<template>
  <div>
    <h1>Consumption</h1>
    <form @submit.prevent="addNewTodo">
      <label>new todo</label>
      <input v-model="state.newTodo" name="newTodo"/>
      <button>Add Todo</button>
    </form>
    <!-- <pre>{{ state.newTodo }}</pre> -->
    <ul>
      <div v-for="(todo,index) in state.todos" v-bind:key="todo.id" class="todo">
        <h3 @click="toggleDone(todo)" v-bind:class="{ done:todo.done }">{{ todo.content }}</h3>
        <button @click="removeTodo(index)">-erase-</button>
      </div>
    </ul>
  </div>
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {

    let state = reactive({
      newTodo : '',
      todos : [],
    });

    function addNewTodo() {
      console.log(state.newTodo);
      state.todos.push({
        id: Date.now(),
        done : false,
        content : state.newTodo,
      });
      state.newTodo = '';
    }

    function toggleDone(todo) {
      todo.done = !todo.done;
      console.log(todo.done);
    }

    function removeTodo(index) {
      console.log('erased todo at: , index')
      state.todos.splice(index,1);
    }

    return {
      state,
      addNewTodo,
      toggleDone,
      removeTodo,
    }
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@300&display=swap");
html {
  background: #08070f;
}

.done {
  text-decoration: line-through;
}

.todo {
  cursor : pointer;
}

#app {
  font-family: "IBM Plex Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: greenyellow;
  margin-top: 60px;
}
</style>
