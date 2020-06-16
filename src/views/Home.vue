<template>
  <div>
    {{ name }} {{ password }}
    {{ number }}
  </div>
</template>

<script>
  import { reactive, toRefs, ref } from '@vue/composition-api'

  export default {
    setup(){
      const form = reactive({
        name: 'Othmane',
        password: 'password'
      })
      const number = ref(1000)

      console.log(form)
      console.log(toRefs(form))

      return {
        ...toRefs(form),
        number
      }
    }
  }
</script>
