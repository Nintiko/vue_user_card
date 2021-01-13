<template>
  <img :src="Val" class="user-photo" />
</template>

<script>
export default {
  name: "UserImage",
  props: ["Val"],
};
</script>

<style>
.user-card .user-photo {
  box-sizing: border-box;
  height: 150px;
  margin-top: -100px;
  border-radius: 50%;
  border: 3px solid #ccc;
}
</style>