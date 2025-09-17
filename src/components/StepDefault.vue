<script setup>

import StepDocument from "@/components/StepDocument.vue";

const stepNumber = 6;

</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>

    </template>
  </StepDocument>
</template>