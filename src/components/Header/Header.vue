<template>
  <nav class="nav-bar">
    <a class="logo nav-item" href="#">
      <img src="../../assets/gtlogo.png" alt="logo" />
    </a>
    <div class="header-menu nav-item">
      <ul>
        <li v-for="item in menuItems" :key="item">
          <el-button round
            ><a href="#"> {{ item }} </a></el-button
          >
        </li>
      </ul>
    </div>
    <div class="user-actions nav-item">
      <div>
        <font-awesome-icon icon="bookmark" />
        <font-awesome-icon icon="bell" />
        <font-awesome-icon icon="user-circle" />
      </div>
    </div>
    <div class="hamburger-icon" @click="handleSideDrawer">
      <font-awesome-icon icon="bars" />
    </div>
    <SideDrawer :isSideDrawer="isSideDrawer" :handleOpen="handleSideDrawer" />
    <div class="overlay" v-if="isSideDrawer" @click="handleSideDrawer"></div>
  </nav>
</template>

<script>
import SideDrawer from "../SideDrawer/SideDrawer.vue";
export default {
  name: "Header",
  components: {
    SideDrawer,
  },
  data() {
    return {
      menuItems: ["Discover", "Create", "Download"],
      isSideDrawer: false,
    };
  },
  methods: {
    handleSideDrawer() {
      this.isSideDrawer = !this.isSideDrawer;
    },
  },
};
</script>
<style>
@import "./Header.css";
</style>