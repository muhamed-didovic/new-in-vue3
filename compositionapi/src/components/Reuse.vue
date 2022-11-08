<template>
  <div>
    {{ x }} {{ y }}
  </div>
</template>

<script>
  import { useMousePosition } from '../mouse.js'

  export default {
    setup () {
      const { x, y } = useMousePosition()

      return {
        x,
        y
      }
    }
  }
</script>
