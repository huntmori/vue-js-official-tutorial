<script setup>
import {reactive, ref} from 'vue'

// 컴포넌트 로직
// 여기에 반응형 상태를 선언합니다.
const text = ref("Hello vue");
const counter = reactive({
  count: 0
})
</script>

<script>
  export default {
    name: 'Step002View'
  };
</script>
<template>
  <div>
    <hr>
    <a href="https://v3-docs.vuejs-korea.org/tutorial/#step-2">
      Step2 - document
    </a>
    <br>
    <h1>{{ text }}</h1>
    <p>
      숫자세기 : {{counter.count}}
    </p>
    <hr>
  </div>
</template>