<template>
  <ul>
    <li v-for="(todo, index) in todos" :key="index" :class="{ done: todo.done }">
      {{ todo.text }}
      <button @click="$emit('toggle', index)">✓</button>
      <button @click="$emit('delete', index)">✕</button>
    </li>
  </ul>
</template>

<script setup>
defineProps(['todos'])
defineEmits(['delete', 'toggle'])
</script>

<style scoped>
.done {
  text-decoration: line-through;
  color: gray;
}
</style>
