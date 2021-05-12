<template>
  <div class="check-list-wrapper">
    <div class="check-list-container">
      <h3>CheckList</h3>
      <div class="check-list-items">
        <div
          class="check-list-item"
          v-for="item in checkListItem"
          :key="item.value"
          :class="{ checked: !item.checked }"
          @click="item.checked = !item.checked"
        >
          <span>{{ item.value }}</span>
          <font-awesome-icon
            icon="check-circle"
            class="check-green"
            v-if="item.checked"
          />
        </div>
        <el-button round class="check-box-button">Preview</el-button>
        <el-button type="primary" round class="check-box-button"
          >Publish</el-button
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CheckList",
  data() {
    return {
      checkListItem: [
        {
          value: "Name",
          checked: true,
        },
        {
          value: "Description",
          checked: true,
        },
        {
          value: "Cover photo",
          checked: true,
        },
        {
          value: "At least 1 point",
          checked: true,
        },
        {
          value: "Narration",
          checked: false,
        },
        {
          value: "Category",
          checked: false,
        },
      ],
    };
  },
};
</script>
<style>
@import "./CheckList.css";
</style>