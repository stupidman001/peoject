<template>
  <div
    class="YUJUN-switch"
    :class="{ 'is-checked': value }"
    @click="handleClick"
  >
    <span class="YUJUN-switch__core" ref="core">
      <span class="YUJUN-switch__core--button"></span>
    </span>
    <input type="checkbox" class="YUJUN-switch_input" :name="name" ref="input">
  </div>
</template>

<script>
export default {
  props: {
    // 是否选中状态
    value: {
      type: Boolean,
      default: false,
    },
    // 开启 / 关闭 背景颜色
    activeColor: {
      type: String,
      default: "",
    },
    inactiveColor: {
      type: String,
      default: "",
    },
    name: {
      type: String,
      defualt: ''
    }
  },
  methods: {
    handleClick() {
      this.$emit("input", !this.value);
      this.$refs.input.checked = this.value
    },
  },
  watch: {
    value() {
      if (this.activeColor || this.inactiveColor) {
        if (this.value) {
          this.$refs.core.style.borderColor = this.activeColor;
          this.$refs.core.style.backgroundColor = this.activeColor;
        } else {
          this.$refs.core.style.borderColor = this.inactiveColor;
          this.$refs.core.style.backgroundColor = this.inactiveColor;
        }
      }
    },
  },
  mounted() {
    if (this.activeColor || this.inactiveColor) {
      if (this.value) {
        this.$refs.core.style.borderColor = this.activeColor;
        this.$refs.core.style.backgroundColor = this.activeColor;
      } else {
        this.$refs.core.style.borderColor = this.inactiveColor;
        this.$refs.core.style.backgroundColor = this.inactiveColor;
      }
    }
    this.$refs.input.checked = this.value
  },
};
</script>

<style lang="scss" scoped>
@import "./index.scss";
</style>