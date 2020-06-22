<template>
  <div>
    {{ number }}
  </div>
</template>

<script>
  import { ref, watchEffect, watch, reactive, toRefs } from '@vue/composition-api'
 
  export default {
    setup(){
      // using ref()
      // const number = ref(0)

      // setInterval( () => {
      //   number.value ++
      // }, 1000)

      // watchEffect( () => {
      //   console.log('watchEffect: ' + number.value)
      // })

      // watch( number, (number, previous) => {
      //   console.log('watch: ' + number + ' -  ' + previous)
      // })

      // using reactive
      const state = reactive({
        number: 0
      })

      setInterval( () => {
        state.number ++
      }, 1000)

      watchEffect( () => {
        console.log('watchEffect: ' + state.number)
      })

      // watch( () => state.number, (number, previous) => {
      //   console.log('watch: ' + number + ' -  ' + previous)
      // })

      watch(() => state, (state) => {
        console.log('changed ' + state.number)
      }, {
        deep: true
      })

      return toRefs(state)
    }
  }
</script>
  