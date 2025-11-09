<script setup>
import { ref } from 'vue'

const tasks = ref([
  { id: 1, title: 'покупки', text: 'хлеб, молоко, яйца' },
  { id: 2, title: 'домашка', text: 'мдк, экономика' },
  { id: 3, title: 'прогулка', text: 'погулять с подругой' },
  { id: 4, title: 'работа', text: 'ответить клиентам' }
])
</script>

<template>
  <div class="app">
    <h1>Список дел</h1>
    <div class="tasks">
      <div v-for="task in tasks" :key="task.id" class="task">
        <h3>{{ task.title }}</h3>
        <p>{{ task.text }}</p>
      </div>
    </div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f5f7fa;
  padding: 20px;
}

.app {
  max-width: 600px;
  margin: 0 auto;
}

h1 {
  text-align: center;
  color: #2c3e50;
  margin-bottom: 30px;
}

.tasks {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.task {
  background: white;
  padding: 16px;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.task h3 {
  color: #3498db;
  margin-bottom: 8px;
}

.task p {
  color: #555;
  line-height: 1.5;
}
</style>