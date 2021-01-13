<template>
  <div class="user-card">
    <UserImage :Val="userCardInfo.Image" />
    <UserNickname :Nick="userCardInfo.Nickname" />
    <UserName
      :firstName="userCardInfo.FirstName"
      :lastName="userCardInfo.LastName"
    />
    <UserLine />
    <UserInfo ImageVal="./img/location.png" :TextVal="userCardInfo.Address" />
    <UserInfo ImageVal="./img/mail.png" :TextVal="userCardInfo.Email" />
    <UserInfo ImageVal="./img/phone.png" :TextVal="userCardInfo.Phone" />
  </div>
</template>

<script>
import UserImage from "./UserImage.vue";
import UserNickname from "./UserNickname.vue";
import UserName from "./UserName.vue";
import UserLine from "./UserLine.vue";
import UserInfo from "./UserInfo.vue";

export default {
  name: "UserCard",
  components: {
    UserImage,
    UserNickname,
    UserName,
    UserLine,
    UserInfo,
  },
  props: ["userCardInfo"],
};
</script>

<style>
.user-card {
  width: 300px;
  padding: 20px;
  border-radius: 10px;
  margin-top: 100px;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #2c3e50;
  box-shadow: 0 0 15px 0 rgba(50, 50, 50, 0.2);
  text-align: center;
}
</style>