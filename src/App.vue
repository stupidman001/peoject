<template>
  <div>

    <!-- <Button>按钮组件</Button>
    <Button type="primary">按钮组件</Button>
    <Button type="success">按钮组件</Button>
    <Button type="warning">按钮组件</Button>
    <Button type="danger">按钮组件</Button>
    <Button type="info">按钮组件</Button>

    <Button plain>镂空按钮</Button>
    <Button type="primary" plain>镂空按钮</Button>
    <Button type="success" plain>镂空按钮</Button>
    <Button type="warning" plain>镂空按钮</Button>
    <Button type="danger"  plain>镂空按钮</Button>
    <Button type="info"    plain>镂空按钮</Button>

    <Button round>圆角按钮</Button>
    <Button type="primary" round>圆角按钮</Button>
    <Button type="primary" plain round>圆角按钮</Button>

    <Button circle></Button>
    <Button type="primary" circle></Button>
    <Button type="primary" plain circle></Button>

    <Button icon="huodongyunying">图标按钮</Button>
    <Button icon="dingdanguanli">图标按钮</Button>
    <Button icon="leimuguanli">图标按钮</Button>

    <Button circle></Button>

    <Button @click="fun">执行函数</Button>

    <Button icon="leimuguanli" circle></Button> -->
    
    <Dialog />

  </div>
</template>

<script>
// 导入组件
// import Button from '@/components/Button'
import Dialog from '@/components/Dialog'

export default {
  name: 'App',
  components:{
    // Button,
    Dialog
  },
  methods:{
    fun(){
      console.log('函数执行了')
    }
  }
}
</script>

<style lang="scss">
  @import "@/assets/css/common.scss";
</style>