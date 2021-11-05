<template>
  <div class="afsAlert" v-show="visible">
    <div class="yindao-alert" v-if="visible">
      <div class="header">
        <span aria-hidden="true" class="close" @click="close">&times;</span>
        <div class="title">为了更高效的操作，请选择售后运营模式</div>
      </div>

      <div class="body">
        <div
          class="item"
          v-for="(item, index) in infos"
          :key="index"
          @click="check(index)"
          :class="{ 'is-checkedItem': index === currentCheck }"
        >
          <div
            class="model_title"
            :class="{ 'is-checked': index === currentCheck }"
          >
            {{ item.title }}
          </div>
          <div class="model_introduce">模式介绍</div>
          <div class="introduce_content">{{ item.introduceContent }}</div>
          <div class="content_title">模式内容</div>
          <div class="model_content">{{ item.modelContent }}</div>
          <div class="check">查看示意</div>
        </div>
      </div>

      <div class="footer">
        <button @click="submit">确定选择该模式</button>
        <span>去「售后配置-运营模式」自定义设置模式内容</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "yindao-alert",
  data() {
    return {
      visible: true,
      infos: [
        {
          title: "简单模式",
          introduceContent:
            "简单模式适用于店铺人员规模小，单量较少，一人多角色方式运营店铺。",
          modelContent: "状态页签合并",
        },
        {
          title: "标准模式",
          introduceContent:
            "标准模式适用于售后人员规模中等，客服专职处理售后单据的店铺。",
          modelContent: "状态页签不合并启用批量导入执行功能",
        },
        {
          title: "高级模式",
          introduceContent:
            "高级模式适用于售后人员规模较大，单量较多，客服需要分单处理等精细化运营的店铺。",
          modelContent:
            "状态页签不合并启用批量导入执行功能启用服务单分单/领单功能",
        },
      ],
      // 选中状态
      checked: false,
      currentCheck: -1,
    };
  },
  methods: {
    close() {
      this.visible = false;
    },
    check(index) {
      if (this.currentCheck == index) {
        this.currentCheck = -1;
        return;
      }
      this.currentCheck = index;
    },
    submit() {
      if (this.currentCheck == -1) return;
      else alert(this.currentCheck);
    },
  },
};
</script>

<style lang="css" scoped>
.afsAlert{
    width:100%;
    height: 100%;
    background: rgba(0,0,0,0.65);
    position: fixed;
    top: 0; 
    left: 0;
}
.yindao-alert {
  margin: 244px auto;
  width: 782px;
  height: 420px;
  background: #ffffff;
  border-radius: 2px;
  position: relative;
  margin: 224px auto;
}

/* 弹框头部 */
.yindao-alert .header {
  height: 74px;
}
.yindao-alert .header .close {
  position: absolute;
  right: 15px;
  top: 14px;
  width: 9px;
  height: 9px;
  font-size: 20px;
  color: #979797;
}
.yindao-alert .header .close:hover {
  cursor: pointer;
}

.yindao-alert .header .title {
  font-size: 16px;
  font-weight: 600;
  position: absolute;
  left: 233px;
  top: 31px;
}
/* 弹框头部完 */

/* 内容部分 */
.yindao-alert .body {
  display: flex;
  justify-content: space-between;
  padding: 0 26px;
}
.yindao-alert .body .item {
  width: 234px;
  height: 278px;
  border: 1px solid rgba(215, 221, 228, 1);
  box-sizing: border-box;
  padding: 24px 20px 16px 20px;
  text-align: center;
}
.yindao-alert .body .item:hover {
  cursor: pointer;
  background: rgba(245, 247, 249, 1);
  border: 1px solid rgba(51, 153, 255, 1);
}
.yindao-alert .body .item .model_title {
  font-weight: 600;
  margin-bottom: 31px;
}
.yindao-alert .body .item .model_introduce {
  font-weight: 500;
  font-size: 12px;
}
.yindao-alert .body .item .introduce_content {
  font-size: 12px;
  color: rgba(109, 114, 120, 1);
  margin-top: 5px;
  margin-bottom: 15px;
  height: 54px;
}
.yindao-alert .body .item .content_title {
  font-weight: 500;
  font-size: 12px;
  margin-bottom: 5px;
}
.yindao-alert .body .item .model_content {
  font-size: 12px;
  color: rgba(109, 114, 120, 1);
  height: 54px;
}
.yindao-alert .body .item .check {
  font-size: 12px;
  color: rgba(51, 153, 255, 1);
  font-weight: normal;
}
/* 内容部分完 */

/* 底部 */
.yindao-alert .footer {
  margin-top: 20px;
}
.yindao-alert .footer button {
  margin-left: 331px;
}
.yindao-alert .footer span {
  font-size: 12px;
  color: rgba(51, 153, 255, 1);
  padding-left: 17px;
}
.yindao-alert .footer span:hover {
  cursor: pointer;
}
/* 底部完 */

/* 选中状态 */
.yindao-alert .is-checked {
  color: rgba(51, 153, 255, 1);
}
.yindao-alert .is-checkedItem {
  background: rgba(245, 247, 249, 1);
  border: 1px solid rgba(51, 153, 255, 1);
}
</style>