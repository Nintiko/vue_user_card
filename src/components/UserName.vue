<template>
  <p class="user-name">{{ firstname + " " + lastName }}<br /></p>
</template>

<script>
export default {
  name: "UserName",
  props: ["firstName", "lastName"],
};
</script>

<style>
.user-card .user-name {
  font-size: 30px;
  font-weight: 900;
  line-height: 1.4;
  margin: 5px 0;
}
</style>