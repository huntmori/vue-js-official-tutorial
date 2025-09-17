<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'StepDocument',
  props: {
    href: { type: String, required: true },
    target: { type: String, default: '_self' },
    rel: { type: String, default: undefined }
  }
})
</script>

<template>
  <hr>
  <p>
    <a :href="href" :target="target" :rel="rel">
      <slot name="link">링크</slot>
    </a>
  </p>
  <div class="result">
    <slot name="result" />
  </div>
  <hr>
</template>