<template>
  <div v-if="show">
      <div>这个是组件中的内容</div>
      <button @click="fn">点击按钮</button>
  </div>
</template>

<script>
export default {
    data(){
        return {
            show:true
        }
    },
    methods:{
        fn(){
            this.show = !this.show
        }
    }
}
</script>