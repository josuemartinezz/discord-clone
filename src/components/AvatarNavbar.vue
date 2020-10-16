<template>
  <div class="avatar-menu">
    <slot> </slot>
  </div>
</template>

<script>
export default {
  name: "AvatarNavbar",
};
</script>

<style lang="less" scoped>
.avatar-menu {
  z-index: 2;
  position: relative;
  height: 100vh;
  left: 0;
  background-color: rgba(var(--avatar-sidebar));
  max-width: 72px;
  min-width: 72px;
  overflow: auto;
  display: flex;
  align-items: center;
  flex-direction: column;
}
::-webkit-scrollbar {
  width: 0px;
}
</style>