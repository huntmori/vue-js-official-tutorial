<script>
import {defineComponent} from "vue";

// eslint-disable-next-line vue/no-export-in-script-setup
export default defineComponent({
  name: 'ChildComponentDefault',
  props: {
    greeting: { type: String, require: false }
  }
})

</script>

<template>
  {{
    greeting
    ? greeting
    : 'prop이 아직 전달되지 않앗습니다.'
  }}
</template>

<style scoped>

</style>