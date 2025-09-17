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
  <div class="col">
    <div class="col-content">
      <p>
        <a :href="href" :target="target" :rel="rel">
          <slot name="link">링크</slot>
        </a>
      </p>
    </div>
    <div class="result col-content" style="width: 100%">
      <slot name="result" />
    </div>
  </div>
</template>