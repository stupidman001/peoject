<template>
  <div>
      <slot name="header"></slot>
      <slot name="body"></slot>
      <slot name="footer"></slot>
      <slot></slot>
  </div>
</template>

<script>
export default {
    created(){
        console.log(this)
    }
}
</script>

<style>

</style>