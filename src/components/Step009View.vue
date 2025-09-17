<script setup>

import StepDocument from "@/components/StepDocument.vue";
import {onMounted, ref} from 'vue'

const stepNumber = 9;

const p = ref(null)

onMounted(() => {
  p.value.textContent = '마운트 되었어요!';
});

</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>
      <p ref="p">안녕</p>
    </template>
  </StepDocument>
</template>