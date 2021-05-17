<template>
  <div id="app">
    <Header />
    <div class="page-wrapper">
      <Description />
      <div>
        <ContentTab />
        <PlaceTags />
        <Categories />
      </div>
      <CheckList />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header/Header.vue";
import ContentTab from "./components/ContentTab/ContentTab.vue";
import PlaceTags from "./components/PlaceTags/PlaceTags.vue";
import Categories from "./components/Categories/Categories.vue";
import Description from "./components/Description/Description.vue";
import CheckList from "./components/CheckList/CheckList.vue";

export default {
  name: "App",
  components: {
    Header,
    ContentTab,
    PlaceTags,
    Categories,
    Description,
    CheckList,
  },
};
</script>

<style>
#app {
  font-family: "Lato", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  max-width: 90%;
  margin: 0 auto;
}
.page-wrapper {
  display: flex;
}
@media (max-width: 767.98px) {
  #app {
    max-width: 100%;
  }
  .page-wrapper {
    flex-direction: column;
  }
  .header-menu,.user-actions {
    display: none;
  }
}
</style>
