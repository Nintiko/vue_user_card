<template>
  <div id="app">
    <UserCard :userCardInfo="UserCardInfo" />
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
};
</script>

<style>
</style>
