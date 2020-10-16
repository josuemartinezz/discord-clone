<template>
  <div class="user-item">
    <div class="content">
      <div class="img">
        <slot name="image"></slot>
      </div>
      <div class="username">
        <slot name="username"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "UserItem",
  props: {
    isChannel: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="less" scoped>
.user-item {
  width: 100%;
  .content {
    border-radius: 4px;
    margin-left: 10px;
    margin-top: 2px;
    cursor: pointer;
    padding-top: 7px;
    padding-bottom: 7px;
    padding-left: 10px;
    color: rgba(var(--text-channel-item));
    display: flex;
    align-items: center;
    padding: 10 8px;
    .img {
      margin-right: 12px;
    }
    &:hover {
      background-color: rgba(52, 55, 60);
      .content {
        .username {
          color: white;
        }
      }
    }
  }
}
</style>