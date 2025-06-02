<template>
  <form @submit.prevent="submitTask">
    <input v-model="newTask" placeholder="Нове завдання" />
    <button type="submit">Додати</button>
  </form>
</template>

<script setup>
import { ref } from 'vue'
const emit = defineEmits(['add'])
const newTask = ref('')

function submitTask() {
  if (newTask.value.trim()) {
    emit('add', newTask.value.trim())
    newTask.value = ''
  }
}
</script>
