<template>
  <button
    class="YUJUN-button"
    :class="[
      `YUJUN-button__${type}`,
      { isplain: plain, isround: round, iscircle: circle },
    ]"
    @click="handleClick"
  >
    <i v-if="icon" :class="`iconfont icon-${icon}`"></i>
    <!-- 按钮的内容 -->
    <span v-if="$slots.default"><slot></slot></span>
  </button>
</template>

<script>
export default {
  name: "YUJUN-button",
  props: {
    type: {
      type: String,
      default: "",
    },
    plain: {
      type: Boolean,
      default: false,
    },
    round: {
      type: Boolean,
      default: false,
    },
    circle: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    icon: {
      type: String,
      default: "",
    },
  },
  created(){
    console.log(this)
  },
  methods: {
    handleClick() {
      this.$emit("click");
    },
  },
};
</script>

<style src="@/assets/font/iconfont.css">
</style>
<style lang="scss" scoped>
@import "./Button.scss";
</style>