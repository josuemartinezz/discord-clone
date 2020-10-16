<template>
  <div class="channel-sidebar">
    <div class="header">
      <slot name="header"></slot>
    </div>
    <div class="body">
      <slot name="body"></slot>
    </div>
    <div class="footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChannelSidebar",
  
};
</script>

<style lang="less" scoped>
::-webkit-scrollbar {
  width: 5px;
}
::-webkit-scrollbar-track {
  background: transparent;
}
::-webkit-scrollbar-thumb {
  background: rgba(32, 34, 37);
  border-radius: 50px;
}
.channel-sidebar {
  z-index: 2;
  font-weight: normal;
  position: relative;
  min-width: 240px;
  background-color: rgba(var(--channel-sidebar));
  height: 100vh;
  overflow: auto;
  .footer {
    position: fixed;
    bottom: 0px;
    width: 100%;
    background-color: rgba(41, 43, 47);
    height: 52px;
    display: flex;
    align-items: center;
    width: 240px;
    .content {
      padding-left: 20px;
    }
  }
  .body {
    display: flex;
    flex-direction: column;
  }
  .header {
    height: 48px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-left: 16px;
    color: white;
    padding-right: 16px;
    cursor: pointer;
    transition: all 0.25s ease;
    &:hover {
      background-color: rgba(52, 55, 60);
    }
  }
}
</style>