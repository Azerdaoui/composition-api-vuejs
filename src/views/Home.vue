<template>
  <div>
    <div v-for="user in users" :key="user.id">{{ user.name }}</div>
  </div>
</template>

<script>
  import { reactive, onMounted, toRefs } from '@vue/composition-api'

  export default {
    setup(){
      const state = reactive({
        users: [],
      })

      function getUsers() { 
        state.users = [{id: 1, name: 'Othmane'}, {id: 2, name: 'Alex'}]
      }

      onMounted ( () => {
        getUsers()
      })

      return {
        ...toRefs(state)
      }
    }
  }
</script>
  