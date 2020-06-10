<template>
  <div>
    {{ number }}
    {{ string }}
  </div>
</template>

<script>
  import { ref } from '@vue/composition-api'

  export default {
    setup(){
      let number = ref(0)
      let string = ref('abc')

      setInterval(() => {
        number.value++
      }, 1000)

      return{
        number,
        string
      }
    }
  }
</script>
