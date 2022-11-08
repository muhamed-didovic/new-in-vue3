<template>
  <div>
    {{ todos }}
  </div>
</template>

<script>
  import axios from 'axios'

  export default {
    async setup () {
      const todos = await axios.get('https://jsonplaceholder.typicode.com/todos')

      return {
        todos
      }
    }
  }
</script>