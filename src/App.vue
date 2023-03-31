<script setup>
import { onMounted, ref } from 'vue'
import Header from './components/Header.vue';
import MainHeader from './components/MainHeader.vue';
const todos = ref([])
const todo = ref('')

function CreateTodo() {
  todos.value.push(todo.value)
  todo.value = ''
}

function deleteTodo(index) {
  todos.value.splice(index, 1)
}

onMounted( () =>{
  console.log("hello")
})
</script>

<template>
  <div class="wrapper">
    <Header />
    <main class="main">
      <MainHeader />
      <textarea v-model="todo" name="" id="" cols="30" rows="10"></textarea>
      <button @click="CreateTodo">Create todo</button>

      <h2 class="title">
        All Todo List
      </h2>

      <ol>
        <li v-for="todo, i in todos" :key="i" @click="deleteTodo">
        {{ todo }}<button class="delete">Delete</button>
           </li>
      </ol>
      

  </main>
  </div>
</template>

<style scoped>

main {
  display: flex;
  flex-direction: column;
  max-width: 50vw;
  margin: 0 auto;
}

.title {
  text-align: center;
  margin-bottom: 1rem;
  color: salmon;
  font-size: 0.9rem;
}

main {
  display: flex;
  flex-direction: column;
  max-width: 50vw;
  margin: 0 auto;
}

.main textarea {
  border-radius: 6px;
  resize: none;
  padding: 0.5rem;
}

.main textarea:focus {
  outline: none;
}

.main button {
  width: 10rem;
  height: 3rem;
  margin: 1rem auto 1rem;
  border: none;
  background-color: #eb5755;
  color: #fff;
  border-radius: 6px;
}

button:hover{
           background-color: #000;
}

li {
  
}

.main .delete {
  width: 4rem;
  height: 2rem;
  margin-left: 4rem;
  border: none;
  color: #fff;
  border-radius: 6px;
}
</style>



