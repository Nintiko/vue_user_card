<template>
  <p class="user-info-item">
    <img :src="ImageVal" />
    {{ TextVal }}
  </p>
</template>

<script>
export default {
  name: "UserInfo",
  props: ["ImageVal", "TextVal"],
};
</script>

<style>
.user-card .user-info-item img {
  vertical-align: middle;
  margin-right: 5px;
}
</style>