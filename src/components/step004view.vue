<script setup>
import { ref } from 'vue'
import StepDocument from "@/components/StepDocument.vue";
const count = ref(0)

const increment = function() {
  count.value++
}
</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument href="https://v3-docs.vuejs-korea.org/tutorial/#step-4">
    <template #link>
      Step4 - Document
    </template>
    <template #result>
      <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
      <button @click="increment">숫자 세기: {{ count }}</button>
    </template>
  </StepDocument>
</template>

<script>
  export default {
    name: 'Step004View'
  }
</script>