<template>
  <div class="YUJUN-input">
    <input
      class="YUJUN-input__inner"
      :class="{ 'is-disabled': disabled }"
      :placeholder="placeholder"
      :type="type"
      :name="name"
      :disabled="disabled"
    />
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
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
  @import "./index.scss";
</style>