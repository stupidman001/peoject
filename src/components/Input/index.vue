<template>
  <div class="YUJUN-input">
    
    <input
      class="YUJUN-input__inner"
      :class="{ 'is-disabled': disabled }"
      :placeholder="placeholder"
      :type="showPassword ? (passwordVisible ? 'text' : 'password') : type"
      :name="name"
      :disabled="disabled"
      :value="value"
      @input="handleInput"
    />

    <!-- 清除按钮、显示密码 按钮 -->
    <span>
      <i v-if="clearable && value" @click="clear">清除</i>
      <i v-if="showPassword && type == 'password'" @click="handlePassword">显示</i>
    </span>

  </div>
</template>

<script>
export default {
  name: "YUJUN-input",
  components: {},
  props: {
    placeholder: {
      type: String,
      default: "",
    },
    type: {
      type: String,
      default: "text",
    },
    name: {
      type: String,
      default: "",
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    value: {
      type: String,
      default: "",
    },
    clearable: {
      type: Boolean,
      default: false,
    },
    showPassword: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      // 显示是否显示密码框
      passwordVisible: false
    };
  },
  methods: {
    handleInput(e) {
      this.$emit("input", e.target.value);
    },
    // 清除输入框内容
    clear() {
      this.$emit("input", "");
    },
    // 密码的显示
    handlePassword() {
      this.passwordVisible = !this.passwordVisible
    }
  }
};
</script>

<style lang="scss" scoped>
  @import "./index.scss";
</style>