<template>
  <p>{{ text }} is now {{ uppercase }}</p>
</template>

<script>
  import { computed } from 'vue'

  export default {
    props: {
      text: {
        required: true,
        type: String
      }
    },
    
    setup (props) {
      const uppercase = computed(() => props.text.toUpperCase())

      return {
        uppercase
      }
    }
  }
</script>
