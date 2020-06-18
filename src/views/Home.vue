<template>
  <div>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
    {{ number }}
  </div>
</template>

<script>
  import { ref } from '@vue/composition-api'

  export default {
    setup(){
      const number = ref(0)

      function increment () {
        number.value++
      } 
      function decrement () {
        number.value--
      }

      return {
        number,
        increment,
        decrement
      }
    }
  }
</script>
