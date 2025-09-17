<script setup>

import {ref, watch} from 'vue'
import StepDocument from "@/components/StepDocument.vue";

const stepNumber = 10;

const todoId = ref(1)
const todoData = ref(null)

async function fetchData() {
  todoData.value = null
  const res = await fetch(
      `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
  )
  todoData.value = await res.json()
  console.log(todoData.value)
}

async function clickHandler() {
  todoId.value++;
}

watch(todoId, () => {
  fetchData();
})

fetchData()
</script>

<template>
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>
      <p>할 일 id: {{ todoId }}</p>
      <button @click="clickHandler">다음 할 일 가져오기</button>
      <p v-if="!todoData">로딩...</p>
      <pre v-else>{{ todoData }}</pre>
    </template>
  </StepDocument>
</template>