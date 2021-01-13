<template>
  <div id="app">
    <UserCard/>
  </div>
</template>

<script>
import UserCard from './components/UserCard.vue'

export default {
  name: 'App',
  components: {
    UserCard
  },
  data(){
    return {
      UserCardInfo:{
        Image : "",
        Nickname: "lol",
        FirstName: "MyFirstName",
      }
    }
  },
}
</script>

<style>

</style>
