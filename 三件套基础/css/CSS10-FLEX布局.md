### <u>**CSS10-FLEX布局**</u>

flex弹性盒子会清除浮动、clear、和vertical-align属性的效果

所有flex容器的子元素都是flex项目

`flex-direction`主轴方向<br>`justify-content` 子元素排列方式<br>`flex-wrap`设置是否换行<br>`align-content`设置侧轴上的子元素排列（多行）<br>`align-items`设置侧轴上的子元素排列（单行）<br>`flex-flow`复合`flex-direction`和`flex-wrap`

###### 1、主轴方向

row从左到右 row-reverse反转 column 主轴为y轴（此时x为侧轴）

###### 2、justify-content属性值

flex-start(默认)从主轴头部开始

flex-end从尾部开始  center居中 space-around 平摊 space-between  两边贴边再平摊

###### 3、`flex-wrap` 

flex默认不换行，会进行挤压

###### 4、`align-items` 

center挤在一起居中stretch拉伸（默认）flex由上至下

5、`align-content` 同理