<template>
  <div class="user-card">
      <UserImage/>
  </div>
</template>

<script>
import UserImage from './UserImage.vue'

export default {
  name: "UserCard",
  components: {
      UserImage,
  },
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