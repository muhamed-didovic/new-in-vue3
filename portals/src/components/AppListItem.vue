<template>
  <div>
    <a href="#" @click.prevent="confirm = true">Delete</a>

    <AppModal :open="confirm" @yes="deleteItem" @no="confirm = false">
      <div>Are you sure</div>
    </AppModal>
  </div>
</template>

<script>
  import AppModal from './AppModal.vue'

  export default {
    components: {
      AppModal
    },

    data () {
      return {
        confirm: false
      }
    },

    methods: {
      deleteItem () {
        console.log('delete');
        this.confirm = false
      }
    }
  }
</script>