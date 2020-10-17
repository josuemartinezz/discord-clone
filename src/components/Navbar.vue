<template>
  <div class="navbar">
    <div class="content">
      <div class="channel-name">
        <i class="bx bx-hash"></i>
        {{ channel }}
      </div>
      <div class="icons">
        <i class="bx bxs-bell"></i>
        <i class="bx bxs-pin"></i>
        <i class="bx bxs-group"></i>
        <div class="input-search">
          <input type="text" placeholder="Search" />
          <i class="bx bx-search"></i>
        </div>
        <i class="bx bxs-inbox"></i>
        <i class="bx bxs-help-circle"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "navbar",
  props: {
    channel: {
      type: String,
      type: "",
    },
  },
};
</script>

<style lang="less" scoped>
.navbar {
  position: relative;
  //width: 100%;
  height: 48px;
  padding: 0 8px;
  font-size: 16px;
  line-height: 20px;
  cursor: default;
  background-color: rgba(54, 57, 63);
  z-index: 2;
  .content {
    display: flex;
    justify-content: space-between !important;
    align-items: center;
    height: 100%;
    .icons {
      color: rgba(114, 118, 125);
      display: flex;
      align-items: center;
      i {
        margin-left: 7px;
        margin-right: 7px;
        cursor: pointer;
        &:hover {
          color: rgba(220, 221, 222);
        }
      }
      .input-search {
        margin-left: 7px;
        margin-right: 7px;
        position: relative;
        display: flex;
        align-items: center;
        input {
          border-radius: 3px;
          background-color: rgba(32, 34, 37);
          border: none;
          outline: none;
          padding: 5px;
          color: rgba(114, 118, 125);
          &:focus {
            width: 200px;
          }
        }
        i {
          position: absolute;
          right: 0;
          margin-right: 3px;
        }
      }
    }
    .channel-name {
      i {
        margin-left: 24px;
        color: rgba(114, 118, 125);
      }
      color: white;
    }
  }
}
</style>