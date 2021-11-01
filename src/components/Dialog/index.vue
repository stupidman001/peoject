<template>
  <div class="YUJUN-dialog">
    <div class="YUJUN-dialog__header">
      <!-- 标题 -->
      <slot name="title">
        <span class="YUJUN-dialog__header--title"> 
          {{title}}
        </span>
      </slot>
      <!-- 取消按钮 -->
      <button class="YUJUN-dialog__header--btn">X</button>
    </div>
    <!-- 主要内容 -->
    <div class="YUJUN-dialog__body">
      <span>这是一段信息</span>
    </div>
    <!-- 底部操作按钮 -->
    <div class="YUJUN-dialog__footer">
      <Button class="YUJUN-dialog__footer--cancel">取消</Button>
      <Button type="primary" class="YUJUN-dialog__footer--confirm">确定</Button>
    </div>
  </div>
</template>

<script>
import Button from "@/components/Button/index.vue";
export default {
  name: "YUJUN-dialog",
  components: {
    Button,
  },
  props:{
      title:{
        type:String,
        default:''
      }
  }
};
</script>

<style lang="scss" scoped>
@import "./index.scss";
</style>