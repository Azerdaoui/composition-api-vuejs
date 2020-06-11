<template>
  <div>
    {{ name }} {{ password }}
    {{ number }}
  </div>
</template>

<script>
  import { reactive } from '@vue/composition-api'

  export default {
    setup(){
      const form = reactive({
        name: 'Othmane',
        password: 'password'
      })

      return {
        ...form
      }
    }
  }
</script>
