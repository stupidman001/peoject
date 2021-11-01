<template>
  <div>
      <button @click="fn">
          点击按钮
      </button>
  </div>
</template>

<script>
export default {
    methods:{
        fn(){
            this.$emit('update:visible', 200)
        }
    }
}
</script>
