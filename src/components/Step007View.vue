<script setup>

import { ref } from 'vue'
import StepDocument from "@/components/StepDocument.vue";

const stepNumber = 7;

// 각 할 일에 고유한 ID 부여
let id = 0

const newTodo = ref('')
const todos = ref([
  { id: id++, text: 'HTML 배우기' },
  { id: id++, text: 'JavaScript 배우기' },
  { id: id++, text: 'Vue 배우기' }
])

function addTodo() {
  todos.value.push({
    id: id++,
    text: newTodo.value
  })
  newTodo.value = ''
}

function removeTodo(todo) {
  console.log(todo);
  const filtered = todos.value.filter(el => el.id !== todo.id);
  console.log(filtered);
  todos.value = filtered;
}
</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>
      <form @submit.prevent="addTodo">
        <input v-model="newTodo">
        <button>할 일 추가</button>
      </form>
      <ul>
        <li v-for="todo in todos" :key="todo.id">
          {{ todo.text }}
          <button @click="removeTodo(todo)">X</button>
        </li>
      </ul>
    </template>
  </StepDocument>
</template>