<template>
  <div class="channel-sidebar-item">
    <div :class="[`content`, { active: active }]">
      <div class="text">
        <i class="bx bx-hash"></i>
        <slot></slot>
      </div>
      <div class="icons">
        <i class="bx bxs-user-plus"></i>
        <i class="bx bxs-cog"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChannelSidebarItem",
  props: {
    active: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="less">
.channel-sidebar-item {
  width: 100%;
  font-weight: normal;
  .content {
    margin-left: 10px;
    margin-right: 10px;
    margin-top: 2px;
    cursor: pointer;
    padding-top: 7px;
    padding-bottom: 7px;
    color: rgba(var(--text-channel-item));
    font-weight: bold;
    border-radius: 4px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .icons {
      margin-right: 10px;
      display: flex;
      i {
        margin-left: 4px;
      }
      display: none;
    }
    .text {
      font-weight: normal;
      margin-left: 10px;
      display: flex;
      align-items: center;
      i {
        margin-right: 4px;
      }
    }
    &.active {
      background-color: rgba(var(--channel-hover));
      .icons {
        display: flex;
      }
    }
    &:hover {
      background-color: rgba(var(--channel-hover));
      .icons {
        display: flex;
      }
    }
  }
}
</style>