<template>
  <div id="app">
    <UserCard :userCardInfo="UserCardInfo" />
    <button v-on:click="getUserData()" >Обновить</button>
  </div>
</template>

<script>
import UserCard from "./components/UserCard.vue";

export default {
  name: "App",
  components: {
    UserCard,
  },
  data() {
    return {
      UserCardInfo: {
        Image: "",
        Nickname: "",
        FirstName: "",
        LastName: "",
        Address: "",
        Phone: "",
        Email: "",
      },
    };
  },
  methods:{
    getUserData(){
      this.axios.get('http://37.77.104.246/users/getrandom.php')
        .then ((response)=>{
          this.UserCardInfo.Image = response.data.img;
          this.UserCardInfo.Nickname = response.data.email.split('@')[0];
          this.UserCardInfo.FirstName = response.data.firstName;
          this.UserCardInfo.LastName = response.data.lastName;
          this.UserCardInfo.Address = response.data.country + ' ' + response.data.city + ' ' + response.data.street + ' ' + response.data.houseNumber;
          this.UserCardInfo.Phone = response.data.cellPhone;
          this.UserCardInfo.Email = response.data.email;
        })
    }
  },
  mounted(){
    this.getUserData();
  }
};
</script>

<style>
</style>
