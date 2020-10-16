<template>
  <div class="user-avatar">
    <span :class="[`selector`, { active: active }]"
      ><span class="center-point"></span
    ></span>
    <img :src="src" alt="" />
  </div>
</template>

<script>
export default {
  name: "AvatarUser",
  props: {
    src: {
      type: String,
      default: "",
    },
    active: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="less" scoped>
.user-avatar {
  cursor: pointer;
  width: 32px;
  height: 32px;
  position: relative;
  &:hover {
    opacity: 0.8;
  }
  .selector {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 10px;
    height: 10px;
    margin-right: -2px;
    margin-bottom: -2px;
    background-color: rgba(109, 120, 133);
    border-radius: 50px;
    border: solid 3px rgba(41, 43, 47);
    display: flex;
    align-items: center;
    justify-content: center;
    .center-point {
      border-radius: 50px;
      background-color: rgba(41, 43, 47);
      width: 5px;
      height: 5px;
    }
    &.active {
      background-color: rgba(67, 181, 129);
      .center-point {
        position: absolute;
        border-radius: 20px;
        background-color: rgba(67, 181, 129);
        width: 5px;
        height: 5px;
      }
    }
  }
  img {
    width: 100%;
    height: 100%;
    border-radius: 50px;
    object-fit: cover;
  }
}
</style>