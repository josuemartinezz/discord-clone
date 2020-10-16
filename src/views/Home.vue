<template>
  <div class="home">
    
    <!-- <div style="position: relative; flex: 1 1 auto; background: red">Hola</div> -->
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style lang="less">
.home {
  display: flex;
}
.footer-content {
  padding-left: 20px;
  display: flex;
  justify-content: space-between;
  width: 100%;
  align-items: center;
  .icons {
    font-size: 20px;
    color: rgba(185, 187, 190);
    margin-right: 20px;
    i {
      cursor: pointer;
      padding: 5px;
      border-radius: 5px;
      &:hover {
        background-color: rgba(51, 53, 59);
      }
    }
  }
  .user {
    display: flex;
    align-items: center;
    .info {
      margin-left: 13px;
      display: flex;
      flex-direction: column;
      span {
        font-size: 12px;
        color: rgba(185, 187, 190);
      }
      .username {
        cursor: pointer;
        font-size: 14px;
        color: white;
      }
    }
  }
}
</style>
