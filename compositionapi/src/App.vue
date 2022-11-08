<template>
  <div>
    <Reuse />
  </div>
</template>

<script>
  import { ref } from 'vue'
  import Reuse from './components/Reuse.vue'
  
  export default {
    components: {
      Reuse    
    },

    setup () {
      const show = ref(true)

      function destroy() {
        show.value = false
      }

      return {
        show,
        destroy
      }
    }
  }
</script>
