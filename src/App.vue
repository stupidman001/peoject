<template>
  <div>
    <Button type="success" plain  disabled/>
  </div>
</template>

<script>
// 导入组件
import Button from '@/components/Button'

export default {
  name: 'App',
  components:{
    Button
  }
}
</script>

<style lang="scss">
@import "@/assets/css/common.scss";

</style>
