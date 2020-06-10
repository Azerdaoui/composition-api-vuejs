<template>
  <div>
    {{ number }}
  </div>
</template>

<script>
  import { ref } from '@vue/composition-api'

  export default {
    setup(){
      const number = ref(0)

      return{
        number
      }
    }
  }
</script>
