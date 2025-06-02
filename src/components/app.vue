<template>
  <div class="container">
    <h1>Vue ToDo</h1>
    <add-task @add="addTodo" />
    <todo-list :todos="todos" @delete="deleteTodo" @toggle="toggleDone" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import AddTask from './components/AddTask.vue'
import TodoList from './components/TodoList.vue'

const todos = ref([])

function addTodo(task) {
  todos.value.push({ text: task, done: false })
}

function deleteTodo(index) {
  todos.value.splice(index, 1)
}

function toggleDone(index) {
  todos.value[index].done = !todos.value[index].done
}
</script>

<style>
</style>
