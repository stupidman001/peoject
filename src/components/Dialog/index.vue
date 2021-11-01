<template>
  <transition name="YUJUN-dialog-Ani">
    <div
      class="YUJUN-dialog"
      :style="{ width: width, marginTop: top }"
      v-show="visible"
    >
      <div class="YUJUN-dialog__header">
        <!-- 标题 -->
        <slot name="title">
          <span class="YUJUN-dialog__header--title">
            {{ title }}
          </span>
        </slot>
        <!-- 取消按钮 -->
        <button class="YUJUN-dialog__header--btn" @click="handleClose">
          X
        </button>
      </div>
      <!-- 主要内容 -->
      <div class="YUJUN-dialog__body">
        <slot></slot>
      </div>
      <!-- 底部操作按钮 -->
      <div class="YUJUN-dialog__footer" v-if="$slots.footer">
        <!-- 如果footer不传递内容，则不显示footer -->
        <slot name="footer"></slot>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "YUJUN-dialog",
  props: {
    title: {
      type: String,
      default: "",
    },
    width: {
      type: String,
      default: "",
    },
    top: {
      type: String,
      default: "",
    },
    visible: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    handleClose() {
      this.$emit("update:visible", false);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./index.scss";
</style>