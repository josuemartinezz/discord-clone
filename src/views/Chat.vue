<template>
  <div class="home">
    <div class="welcome-message">
      <div class="icon">
        <i class="bx bx-hash"></i>
      </div>
      <div class="text">
        <h1>Welcome to #channelName</h1>
        <small>This is the start of the #nameChannel channel.</small>
        <small><router-link to="">Edit Channel</router-link></small>
      </div>
    </div>
    <div class="send-container">
      <div class="send-message">
        <div class="icon-left">
          <i class="bx bxs-plus-circle bx-sm"></i>
        </div>
        <input type="text" placeholder="Message #channel" />
        <div class="icon-right">
          <i class="bx bxs-gift bx-sm"></i>
          <i class="bx bx-image bx-sm"></i>
          <i class="bx bx-face bx-sm"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style lang="less">
.home {
  .send-container {
    position: absolute;
    bottom: 0;
    width: 100%;
    margin-bottom: 50px;
    .send-message {
      position: relative;
      width: 100%;
      display: flex;
      .icon-right {
        display: flex;
        align-items: center;
        height: 100%;
        position: absolute;
        color: rgba(185, 187, 190);
        right: 0;
        margin-right: 20px;
        i {
          margin-left: 3px;
          margin-right: 3px;
          cursor: pointer;
          &:hover {
            color: rgba(255, 255, 255);
          }
        }
      }
      .icon-left {
        display: flex;
        align-items: center;
        position: absolute;
        color: rgba(185, 187, 190);
        height: 100%;
        margin-left: 25px;
        i {
          cursor: pointer;
          &:hover {
            color: rgba(255, 255, 255);
          }
        }
      }
      input {
        width: 100%;
        padding: 12px;
        padding-left: 50px;
        margin: 10px;
        border-radius: 10px;
        outline: none;
        border: none;
        background-color: rgba(64, 68, 75);
        color: white;
      }
    }
  }
  height: 100vh;
  position: relative;
  background-color: rgba(54, 57, 63);
  .text {
    color: white;
    display: flex;
    flex-direction: column;
    h1 {
      margin-top: 30px;
    }
    small {
      margin-top: 15px;
      color: rgba(181, 179, 182);
      a {
        color: rgba(17, 176, 215);
        text-decoration: none;
      }
    }
  }
  .welcome-message {
    position: absolute;
    bottom: 0;
    padding: 20px;
    margin-bottom: 100px;
    .icon {
      width: 68px;
      height: 68px;
      border-radius: 50%;
      background-color: rgba(69, 69, 69);
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 2rem;
      color: white;
    }
  }
}
</style>
