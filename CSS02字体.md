## CSS02字体和文本

#### 一、字体系列`font-famaly`  `font-size` `font-weight` `font-style` 

```css
p {
    font-family: 'Microsoft Yahei', Arial;
    font-size: 16px;
}
```

​	`font-famaly` 	各个字体之间用英文逗号隔开 有空格的字体加引号<br/>	前面无法显示的字体则使用后面的字体，若都没有则使用浏览器默认字体

​	`font-size`  像素大小（px）

​	`font-weight` 字体粗细 normal（默认，400）bold（700）lighter<br/>	可用normal改变标题等标签的字体粗细

​	`font-style` 字体样式 normal 把斜体字体不倾斜        italic倾斜

#### 二、字体复合属性

`font: font-style font-weight font-size/line-height font-family`

```css
div {
    font: italic 700 16px/20px 'Microsoft Yahei'
}
```

顺序不能颠倒，字号和字体必须出现

三、

文本颜色

​	 `color="green"`或者`color="ff0000"`或`color="f00"`(两两相同的简写)

​	`color=rgb(255,255,0)` rgb即红绿蓝三色程度，使用数字或百分比

​	开发中用得最多的是十六进制

对齐文本

 	`text-align: center`  属性值有center、left、right

装饰文本

​	**`text-decoration: underline;`下划线<br/>	**`text-decoration: none;`默认格式，把链接的下划线去掉<br/>	`text-decoration: overline;`上划线<br/>	`text-decoration: line-through;`删除线

文本首行缩进

 `text-indent: 20px`

 **`text-indent: 2em`文字大小**

行间距

`line-height`文字上下间距之和