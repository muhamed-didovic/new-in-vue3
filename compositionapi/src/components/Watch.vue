<template>
  <div>
    {{ number }}
  </div>
</template>

<script>
  import { ref, watchEffect, watch } from 'vue'

  export default {
    setup () {
      const number = ref(0)

      setInterval(() => {
        number.value += 1
      }, 1000)

      // watchEffect(() => {
      //   console.log(number.value)
      // })

      watch(number, (number, previous) => {
        console.log(`changed from ${previous} to ${number}`)
      })

      return {
        number
      }
    }
  }
</script>