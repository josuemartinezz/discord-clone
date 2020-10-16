<template>
  <div id="app">
    <AvatarNavbar>
      <Avatar icon color="white"></Avatar>
      <Avatar text="T" color="white"></Avatar>
      <Avatar active text="H" color="white"></Avatar>
    </AvatarNavbar>
    <ChannelSidebar>
      <template #header>
        <!-- Aquí recibe el nombre del canal -->
        mr.josue
        <i class="bx bxs-chevron-down"></i>
      </template>
      <template #body>
        <!-- Aquí recibe todos los canales existente -->
        <ChannelSidebarItem active>🎉channel</ChannelSidebarItem>
        <ChannelSidebarItem>🙌 reglas</ChannelSidebarItem>
        <ChannelSidebarItem>🔴 directos</ChannelSidebarItem>
      </template>
      <template #footer>
        <div class="footer-content">
          <div class="user">
            <AvatarUser
              active
              src="https://images.unsplash.com/photo-1503602642458-232111445657?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80"
            ></AvatarUser>
            <div class="info">
              <span class="username">mr.josue</span>
              <span>#6709</span>
            </div>
          </div>
          <div class="icons">
            <i class="bx bxs-microphone"></i>
            <i class="bx bx-headphone"></i>
            <i class="bx bxs-cog"></i>
          </div>
        </div>
      </template>
    </ChannelSidebar>
    <router-view />
    <UserSidebarChannel>
      <template #users>
        <UserItem>
          <template #image>
            <AvatarUser
              active
              src="https://images.unsplash.com/photo-1559969143-b2defc6419fd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=543&q=80"
            ></AvatarUser>
          </template>
          <template #username> mr.josue </template>
        </UserItem>
        <UserItem>
          <template #image>
            <AvatarUser
              active
              src="https://images.unsplash.com/photo-1582731595896-f959c4fb1509?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=678&q=80"
            ></AvatarUser>
          </template>
          <template #username> player1 </template>
        </UserItem>
      </template>
    </UserSidebarChannel>
    <Navbar channel="channel">
    </Navbar>
  </div>
</template>

<script>
import AvatarNavbar from "@/components/AvatarNavbar";
import Avatar from "@/components/Avatar";
import ChannelSidebar from "@/components/ChannelSidebar";
import ChannelSidebarItem from "@/components/ChannelSidebarItem";
import AvatarUser from "@/components/AvatarUser";
import UserSidebarChannel from "@/components/UserSidebarChannel";
import UserItem from "@/components/UserItem";
import Navbar from "@/components/Navbar";
export default {
  name: "app",
  components: {
    AvatarNavbar,
    Avatar,
    ChannelSidebar,
    ChannelSidebarItem,
    AvatarUser,
    UserSidebarChannel,
    UserItem,
    Navbar
  },
};
</script>

<style lang="less">
@import (css)
  url("https://fonts.googleapis.com/css2?family=Merriweather+Sans:wght@300&display=swap");
:root {
  --avatar-sidebar: 32, 34, 37, 1;
  --bg-avatar: 54, 57, 63;
  --hover-avatar: 114, 137, 218;
  --channel-sidebar: 46, 48, 54;
  --channel-hover: 57, 60, 67;
  --text-channel-item: 142, 146, 151;
}
* {
  margin: 0px;
  padding: 0px;
}

body {
  font-family: "Merriweather Sans", sans-serif;
}

#app {
  font-style: normal;
  font-variant: normal;
  line-height: 19.54px;
  display: flex;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
