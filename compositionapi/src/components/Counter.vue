<template>
  <a href="#" @click.prevent="increment">Increment</a> {{ number }}
</template>

<script>
  import { ref } from 'vue'
  
  export default {
    setup () {
      const number = ref(0)

      function increment () {
        number.value++
      }

      return {
        number,
        increment
      }
    }
  }
</script>