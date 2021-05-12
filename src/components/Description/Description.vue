<template>
  <div class="description">
    <h3 class="description-heading">Description</h3>
    <div class="description-options">
      <div class="description-option" v-for="item in options" :key="item.name">
        <h3>{{ item.name }}</h3>
        <ol class="option-items" :class="item.class">
          <li
            class="option-item"
            v-for="(option, index) in item.values"
            :key="index"
          >
            {{ option }}
          </li>
        </ol>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Description",
  data() {
    return {
      options: [
        {
          name: "Points",
          values: [
            "Abbesses Metro Station",
            "Pingalle and Moulin R...",
            "Create New Point",
          ],
          class: "points",
        },
        {
          name: "Media",
          values: [],
          class: "media",
        },
        {
          name: "Settings",
          values: [],
          class: "settings",
        },
      ],
    };
  },
};
</script>

<style>
@import "./Description.css";
</style>
