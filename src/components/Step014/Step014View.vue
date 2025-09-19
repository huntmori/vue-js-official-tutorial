<script setup>

import StepDocument from "@/components/StepDocument.vue";
import ChildComp from "./ChildComp.vue";
import { ref } from "vue";

const stepNumber = 14;

const msg = ref('Vue는 개발자에게 정말 유용하죠! 🎁')
</script>

<template>
  <!-- 이 버튼이 작동하도록 만들어 봅시다 -->
  <StepDocument :href="'https://v3-docs.vuejs-korea.org/tutorial/#step-{{stepNumber}}'">
    <template #link>
      Step{{stepNumber}} - Document
    </template>
    <template #result>
      <ChildComp>
        {{ msg }}
      </ChildComp>
    </template>
  </StepDocument>
</template>