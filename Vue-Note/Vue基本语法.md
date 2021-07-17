# Vue.js 基本语法

## Lesson 1 基本功能和指令

Vue2 创建新的Vue app

```javascript
new Vue({
	el:"#root",
    data:{
        // 具体存储的key-value
        exampleKey:exampleValue
    }
     methods: {
        // 方法
    }
})
```

Vue3 格式

```javascript
const newVueApp = {
    data() {
        return {
            // specific data
        	exampleKey:exampleValue
        }
    },
    methods: {
        // 方法
    }
}
Vue.createApp(newVueApp).mount("#root");
```



双括号显示data中元素 `{{  }}` 

```html
<div id="root">
    <h1>
        {{ exampleKey }}
        <!--examplevalue-->
    </h1>
</div>
```

`v-model` 保持更新





#### 插值语法：

在标签体之中使用`{{ }}` 中内含直接填写js表达式

#### 指令语法：

使用`v-bind:`绑定标签的属性，内容填入字符串会被当成**js表达式**执行

`v-bind:title` `v-bind:disabled`  或冒号加属性名简写,可以不写`V-bind`,例如 `:herf`

范例

```html
<button v-bind:disabled="1===0">按钮</button>
```

可自动识别相关语句



`v-bind`  单向数据绑定，数据只能从data流向页面,简写成**冒号**

`v-model` 双向数据绑定，只能用于表单类元素标签，默认收集value值

`v-model:value`可直接简写为`v-model`



### 绑定事件：

`v-on`，简写为`@`

```vue
<button v-on:click="functionName">button</button>
// 或者
<button @click="functionName(%event,参数)">button</button>
```

当对应被绑定的事件被触发时，调用methods中对应的已经定义好的**回调函数名**（参数为事件对象），其中this为vm（箭头函数this为window），使用括号内填写`$event`和其他参数传参

也可以不填函数名直接填写简单的运算式



绑定事件名后面加`.prevent`阻止默认事件 `.stop`阻止事件冒泡 `.once` 事件只触发一次

键盘事件：

常用按键别名 enter esc space tab delete up down left right 



1、Vue实例和容器一一对应

2、真实开发只有一个Vue实例，配合组件使用

### 计算属性

```js
new Vue({
    data:{
	//存放属性    
	},
    computed:{
        // 计算属性
        // getter在propertyName初次被读取和依赖的数值被修改时被调用
        propertyName:{
        	get(){
            }
        }
    }
})


//简写形式
computed:{
    //直接使用函数名作为属性名
    propertyName(){
    
    }
}
```



### 监视属性

```js
watch:{
    propertyName:{
        // 属性发生改变时被调用
        handler(newValue,oldValue){
            // 参数列表传入新旧值
        }，
        immediate:true//默认为false，可让handler立即执行
    }
    // 监视多级结构时用字符串
    'property.subproperty':{
        handler(){}
    }
    // 或者
    ,deep:true
    // 简写同计算属性，用属性名直接作为方法名替代handler
}

// 或者
vm.$watch('properName',{
    // 属性发生改变时被调用
   	handler(newValue,oldValue){
  	// 参数列表传入新旧值
   	}，
    immediate:true//默认为false，可让handler立即执行
})
```



### 绑定样式

`:class`

直接绑定属性名，值为**类名**或**类名的数组**



### 条件渲染

`v-show`

值为false时，元素变为`display:none`，依旧占用dom

`v-if` `v-else`  `v-else-if` 条件语句切换元素

对应为false时不占用dom，完全消失，可以配合`template`使用

### 列表渲染

`v-for`

```html
<div id="fortest">
    <ul v-for="(item,index) in array" :key="item.id">
     	<li>
     		{{ item.text }}
     	</li>
	</ul>
</div>
```

对应数组：

```js
const VueApp = {
    data() {
        return {
            array:[
                { text: 'Learn JavaScript',id: 1
                { text: 'Learn Vue',id:2},
                { text: 'Learn Vue',id:3}
            ]
        }
    }
}
Vue.createApp(VueApp).mount("#fortest")
```

Vue默认key使用index，一般指定数据的唯一标识作为key值如id



### 数组

直接修改数组内的值无法让Vue检测到，需要使用push shift  unshift reverse 等Vue封装好的方法，或者使用Vue.set()方法

### Vue.set() 方法

```js
Vue.set(this.setItem,key,value)
```

### v-model 收集表单数据

单选radio  准备value值

多选框checkbox  准备value值，对应data中准备数组

单个确认checkbox 自动收集checked状态

修饰符

 - lazy 
 - number 
 - trim

### 过滤器

管道符 `|`

`{{ msg | msgFilter }}`

调用`filters`中定义好的`msgFileter`函数，msg传入第一个参数，msgFilter后加括号可以从第二个参数开始追加参数列表



### 生命周期

