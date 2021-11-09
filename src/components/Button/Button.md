参数支持：

参数名           参数描述	                                       参数类型	  默认值
type            按钮类型 primary/success/warning/danger/info      string	default
plain	        是否是朴素按钮	                                   boolean	 false
round	        是否是圆角按钮	                                   boolean	 false
circle	        是否是圆形按钮	                                   boolean	 false
disabled	    是否禁用按钮	                                   boolean	 false
icon	        图标类名	                                       string	 无


事件支持：

事件名	         事件描述
click	        点击事件


父组件使用 Button 绑定了 @click 事件,子组件需要在点击 button 的时候，出发click事件

$slots是一个插槽用来预留位置，default则是指除了具名插槽以外的所有内容














