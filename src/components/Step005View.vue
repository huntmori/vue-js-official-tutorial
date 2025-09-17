<script setup>
import { ref } from 'vue'
import StepDocument from "@/components/StepDocument.vue";

const text = ref('')

function onInput(e) {
  text.value = e.target.value
}
</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument href="https://v3-docs.vuejs-korea.org/tutorial/#step-5">
    <template #link>
      Step5 - Document
    </template>
    <template #result>
      <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
      <div>
        ":value"와 '@input"을 이용한 양방향 바인딩
        <input :value="text" @input="onInput" placeholder="여기에 입력하기">
      </div>
      <div>
        "v-model" 사용
        <input v-model="text" placeholder="여기에 입력하기">
      </div>

      <p>{{ text }}</p>
    </template>
  </StepDocument>
</template>

<script>
export default {
  name: 'Step005View'
}
</script>