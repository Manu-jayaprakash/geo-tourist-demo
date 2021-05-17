<template>
  <div>
    <div class="side-drawer__wrapper" :class="{ open: isSideDrawer }">
      <p @click="handleOpen" class="close-side-drawer">
        <font-awesome-icon icon="times-circle" />
      </p>

      <div class="side-drawer-menu">
        <p v-for="item in menuItems" :key="item">
          <a href="#">
            {{ item }}
          </a>
        </p>
      </div>
      <div class="side-drawer-user-actions">
        <p><font-awesome-icon icon="bookmark" />Bookmarks</p>
        <p><font-awesome-icon icon="bell" />Alerts</p>
        <p><font-awesome-icon icon="user-circle" />Profile</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideDrawer",
  props: ["isSideDrawer", "handleOpen"],
  data() {
    return {
      menuItems: ["Discover", "Create", "Download"],
    };
  },
};
</script>

<style>
@import "./SideDrawer.css";
</style>
