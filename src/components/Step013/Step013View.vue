<script setup>

import StepDocument from "@/components/StepDocument.vue";
import { ref } from 'vue'
import ChildComp from './ChildComp.vue'

const stepNumber = 13;

const childMsg = ref('자식 컴포넌트로부터 아직 메시지를 받지 못했어요!')

</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>
      <ChildComp @response="(msg) => childMsg = msg" />
      {{ childMsg }}
    </template>
  </StepDocument>
</template>