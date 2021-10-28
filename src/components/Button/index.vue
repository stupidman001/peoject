<template>
  <button class="YUJUN-button">按钮组件</button>
</template>

<script>
export default {
  name: "YUJUN-button",
  props: {
    type: {
      type: String,
      default: "default",
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
      type: Boolean,
    },
  },
  created(){
      console.log(this.type,this.plain,this.round,this.circle,this.disabled,this.icon)
  }
};
</script>

<style lang="scss">
</style>