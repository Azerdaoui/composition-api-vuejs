<template>
  <div>
    <User v-for="user in users" :key="user.id" :user="user" />
  </div>
</template>

<script>
  import { ref } from '@vue/composition-api'

  import User from './User'
 
  export default {
    components: {
      User
    },
    
    setup(){
      const users =ref([
        {id: 1, name:'Othmane'},
        {id: 2, name:'Ahmed'}
      ])

      return {
        users
      }
    }
  }
</script>
  