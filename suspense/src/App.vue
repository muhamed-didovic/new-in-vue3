<template>
  <div>
    <div v-if="error">
      Could not load
    </div>
    <Suspense v-else>
      <template #default>
        <TopPosts />
        <LatestPosts />
      </template>
      <template #fallback>
        <div>Loading...</div>
      </template>
    </Suspense>
  </div>
</template>

<script>
  import TopPosts from './components/TopPosts.vue'
  import LatestPosts from './components/LatestPosts.vue'

  import { ref, onErrorCaptured } from 'vue'

  export default {
    components: {
      TopPosts,
      LatestPosts
    },

    setup () {
      const error = ref(false)

      onErrorCaptured(e => {
        error.value = true
        return true
      })

      return {
        error
      }
    }
  }
</script>
