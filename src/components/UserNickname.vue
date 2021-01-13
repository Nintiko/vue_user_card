<template>
  <p class="user-nickname">{{ Nick }}</p>
</template>

<script>
export default {
  name: "UserNickname",
  props: ["Nick"],
};
</script>

<style>
.user-card .user-nickname {
  color: #a0a9b3;
  font-size: 18px;
  margin: 5px 0;
  font-family: monospace;
}
</style>