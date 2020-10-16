<template>
  <div class="channel-users">
    <div class="content">
      <slot name="users"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "UserSidebarChannel",
};
</script>

<style lang="less" scoped>
.channel-users {
  position: absolute;
  right: 0;
  width: 240px;
  background-color: rgba(47, 49, 54);
  height: 100vh;
  .content {
    margin-top: 20px;
    display: flex;
    flex-direction: column;
  }
}
</style>