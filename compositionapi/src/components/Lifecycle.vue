<template>
  <div></div>
</template>

<script>
  import { onMounted, onUnmounted } from 'vue'
  
  export default {
    setup () {
      onMounted(() => {
        console.log('component mounted')
      })

      onUnmounted(() => {
        console.log('component unmounted')
      })
    }
  }
</script>
