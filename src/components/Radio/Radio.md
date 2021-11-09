参数名称	    参数描述	         参数类型	                默认值
v-model	       双向绑定	            布尔类型	               false
label	       单选框和value值	    string，num，Boolean	   ''
name	       name

<Radio v-model="gender" label="0">男</Radio>
<Radio v-model="gender" label="1">女</Radio>

等价于

<Radio @input="label => gender = label" :value="gender" label="0">男</Radio>
<Radio @input="label => gender = label" :value="gender" label="1">女</Radio>

<script>
  data(){
    return {
      gender: '1'
    }
  }
</script>

所以在 Radio 组件中要接收到父组件传来的 value 值，和绑定在自身上的 input 事件
