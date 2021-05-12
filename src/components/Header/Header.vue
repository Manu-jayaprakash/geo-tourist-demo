<template>
  <nav class="nav-bar">
    <a class="logo nav-item" href="#">
      <img src="../../assets/gtlogo.png" alt="logo" />
    </a>
    <div class="header-menu nav-item">
      <ul>
        <li v-for="item in menuItems" :key="item">
          <el-button round>{{ item }}</el-button>
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
  </nav>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      menuItems: ["Discover", "Create", "Download"],
    };
  },
};
</script>
<style>
@import "./Header.css";
</style>