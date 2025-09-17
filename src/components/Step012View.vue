<script setup>

import { ref } from 'vue'
import StepDocument from "@/components/StepDocument.vue";
import ChildComponent012 from "@/components/ChildComponent012.vue";

const stepNumber = 12;

const greeting = ref('부모 컴포넌트로부터 💌을 전달받았어요!')
</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>
      <ChildComponent012 :greeting="greeting"/>
    </template>
  </StepDocument>
</template>