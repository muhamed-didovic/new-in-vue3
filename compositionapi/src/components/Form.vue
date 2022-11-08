<template>
  <form action="#" @submit.prevent="submit">
    <input type="text" v-model="state.form.email">
    <input type="password" v-model="state.form.password">

    <button type="submit">Sign in</button>
  </form>
</template>

<script>
  import { ref, reactive } from 'vue'

  export default {
    setup () {
      const state = reactive({
        form: {
          email: '',
          password: ''
        }
      })

      function submit () {
        console.log(state.form);
      }

      return {
        state,
        submit
      }
    }
  }
</script>