<template>
  <label class="YUJUN-radio" :class="{ 'is-checked': label == value }">
    <span class="YUJUN-radio__input">
      <span class="YUJUN-radio__inner"></span>
      <input
        type="radio"
        class="YUJUN-radio__original"
        :value="label"
        v-model="model"
      />
    </span>
    <span class="YUJUN-radio__label">
      <slot></slot>
      <!-- 如果没有传值，就把label作为文本显示 -->
      <template v-if="!$slots.default">{{ label }}</template>
    </span>
  </label>
</template>

<script>
export default {
  name: "",
  props: {
    label: {
      type: String,
      default: "",
    },
    value:null
  },

  //计算属性
  computed: {
    model: {
      get() {
        return this.value;
      },
      set(value) {
        // 触发父组件的input事件
        this.$emit("input", value);
      },
    },
  },
};
</script>

<style lang="scss" scoped>
  @import "./index.scss";
</style>