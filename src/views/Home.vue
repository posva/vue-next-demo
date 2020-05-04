<template>
  <div class="home">Message: {{ message }}</div>
</template>

<script>
import { defineComponent, computed } from 'vue'

export default defineComponent({
  name: 'Home',
  props: {
    message: {
      required: true,
      type: String,
    },
  },

  setup(props) {
    const name = computed(() => props.message)

    return { name }
  },
})
</script>
