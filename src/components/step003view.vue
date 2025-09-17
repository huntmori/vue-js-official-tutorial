<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
</script>

<template>
  <div>
    <hr>
    <a href="https://v3-docs.vuejs-korea.org/tutorial/#step-3">
      Step3 - document
    </a>
    <h1 :class="titleClass">나를 빨갛게 만들어 보세요</h1> <!-- 여기에 동적 클래스 바인딩 추가 -->
    <hr>
  </div>
</template>

<style>
.title {
  color: red;
}
</style>

<script>
  export default {
    name: 'Step003View'
  }
</script>