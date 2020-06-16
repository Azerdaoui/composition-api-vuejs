<template>
  <div>
    <form>
      <input type="text" v-model="form.name">
      <input type="password" v-model="form.password">
    </form>

    {{ form }}
  </div>
</template>

<script>
  import { ref, reactive } from '@vue/composition-api'

  export default {
    setup(){
      // with ref
      // const name = ref('')
      // const password = ref('')

      // with reactive
      const form = reactive({
        name:'name',
        password:'password'
      })

      const data = { ...form }

      return {
        form,
      }
    }
  }
</script>
