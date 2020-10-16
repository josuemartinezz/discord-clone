<template>
  <div class="navbar">
      <div class="content">
          
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
  width: 100%;
  height: 48px;
  padding: 0 8px;
  font-size: 16px;
  line-height: 20px;
  cursor: default;
  background-color: red;
  z-index: 2;
}
</style>