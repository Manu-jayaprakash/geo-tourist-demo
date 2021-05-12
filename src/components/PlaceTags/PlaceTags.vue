<template>
  <div class="place-tags">
    <h3>Tags</h3>
    <el-input
      class="input-new-tag"
      v-if="inputVisible"
      v-model="inputValue"
      ref="saveTagInput"
      size="mini"
      @keyup.enter.native="handleInputConfirm"
      @blur="handleInputConfirm"
    />
    <el-button v-else class="button-new-tag" size="small" @click="showInput">
      <font-awesome-icon icon="plus" />
    </el-button>
    <el-tag
      class="el-tag-round"
      :key="tag"
      v-for="tag in tags"
      closable
      :disable-transitions="false"
      @close="handleClose(tag)"
    >
      {{ tag }}
    </el-tag>
  </div>
</template>

<script>
export default {
  name: "PlaceTags",
  data() {
    return {
      tags: ["Montmartre", "Paris"],
      inputVisible: false,
      inputValue: "",
    };
  },
  methods: {
    handleClose(tag) {
      this.tags.splice(this.tags.indexOf(tag), 1);
    },
    showInput() {
      this.inputVisible = true;
      this.$nextTick(() => {
        this.$refs.saveTagInput.$refs.input.focus();
      });
    },

    handleInputConfirm() {
      let inputValue = this.inputValue;
      if (inputValue) {
        this.tags.push(inputValue);
      }
      this.inputVisible = false;
      this.inputValue = "";
    },
  },
};
</script>

<style>
@import "./PlaceTags.css";
</style>
