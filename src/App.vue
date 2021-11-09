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

    <!-- 标题 -->
    <!-- <Dialog title="提示!!!">
        <template slot="title">
          <h3 style="color:red">我是标题</h3>
        </template>
    </Dialog> -->

    <!-- 宽度和位置 -->
    <!-- <Dialog
     title="提示!!!"
     width="80%" 
     top="100px"
     :visible.sync="visible"
    >
      弹窗提示!!!
      <template slot="footer">
        <Button>取消</Button>
        <Button>确定</Button>
      </template>
    </Dialog> -->

    <!-- 
    <Input v-model="username" clearable showPassword />
    <Input v-model="username" clearable showPassword type="password" />
     -->

    <!-- <YUJUNSwitch v-model="active" active-color="#13ce66" inactive-color="#ff4949" name="apple" /> -->
    <!-- <YUJUNSwitch @input="fun" :value="active" /> -->

     <!-- <Radio v-model="gender" label="0">男</Radio> -->
     <br>
     <!-- <Radio v-model="gender" label="1">女</Radio> -->
     <br>
     <Radio @input="label => gender = label" :value="gender" label="1">女</Radio>
     <br>
     <Radio @input="label => gender = label" :value="gender" label="0">男</Radio>

  </div>
</template>

<script>
// 导入组件
// import Button from "@/components/Button";
// import Dialog from "@/components/Dialog";
// import Input from "@/components/Input"
// import YUJUNSwitch from "@/components/Switch"
import Radio from "@/components/Radio"

export default {
  name: "App",
  components: {
    Radio
    // Button,
    // Dialog,
    // Input
    // YUJUNSwitch
  },
  data(){
    return {
      gender: '1'
      // username:"用户名称",
      // active:true
    }
  }
};
</script>

<style lang="scss">
  @import "@/assets/css/common.scss";
</style>