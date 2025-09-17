<script setup>

import { ref } from 'vue'
import StepDocument from "@/components/StepDocument.vue";

const stepNumber = 6;

const awesome = ref(true)

function toggle() {
  awesome.value = !awesome.value;
}
</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>
      <button @click="toggle">토글 버튼</button>
      <h1 v-if="awesome">Vue는 굉장해! 엄청나!</h1>
      <h1 v-else>오 안돼 😢</h1>
    </template>
  </StepDocument>
</template>