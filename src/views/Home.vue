<template>
  <div>
    {{ name }} {{ nameShouting }}  <br>
    {{ username }} {{ usernameShouting }}
  </div>
</template>

<script>
  import { ref, computed, reactive, toRefs } from '@vue/composition-api'

  export default {
    setup(){
      const name = ref('Othmane')
      const nameShouting = computed(() => name.value.toUpperCase())

      const state = reactive({
        username: 'Technotic',
        usernameShouting: computed(() => state.username.toUpperCase())
      })

      return {
        name,
        nameShouting,
        ...toRefs(state)
      }
    }
  }
</script>
  