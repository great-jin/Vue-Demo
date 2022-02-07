## 组件
   优点：重用，降低耦合度，减少维护量，组装成复杂应用
### 组件的使用
#### 创建组件
     components 文件夹
	 命名方式：-  my-cmp 推荐
				 MyCmp Vue.component('my-cmp',myCmp)
	1 创建my-cmp组件
	2 引入组件 
	import myCom from '@/components/my-cmp/my-cmp.vue'
	3 注册组件
	  全局注册 main.js 
	  局部注册  在页面components下注册组件
	4 使用组件 
	5 组件可以嵌套
#### 数据传递  A-》B  B->A  父子组件通信 
     1 父子通信
	 props：['messege']
	 数据类型：String 、 Number 、 Boolean 、 Array 、 Object 、 Date 、 Function 、 Symbol ，Promise 任何自定义构造函数、或上述内容组成的数组
	 数据验证：default 默认值 required 必选项 validator 验证   null undifind
	 静态数据
	 动态数据
	 2 子父通信
	  