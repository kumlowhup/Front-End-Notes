CSS笔记01

一、CSS概念

​	Cascading Style Sheets层叠样式表，是用来表现HTML或XML的语言，美化网页，布局页面，可设置文本内容，图片外形、版面外观显示样式。<br/>结构（html）和样式（css）分离<br/>	外部样式表文件扩展名为.css

二、基础语法

```css
h1 {
    color: red;
    font-size: 25px;
}
```

​	选择器与声明（属性及其值）

三、基础选择器

​	1、标签名直接作为选择器：直接选择同一标签名的所有标签

​	2、类选择器 `.类名` 点加类名<br/>		在相对的所需的标签中加入class属性，值为对应的类名<br/>		口诀：样式点定义，结构类调用

​		可以给一个标签加多个类名，两个类名放在一个双引号里 中间用空格隔开

​	3、id选择器 `#id名字` 井号加id名字<br/>		与class选择器方法类似，但是只能被调用一次，一般用于页面唯一性的元素上与js搭配<br/>		口诀：样式#定义，结构id调用

6、通配符选择器，`*` 设置页面中所有标签

四、三种引入方式

​	1、内部样式表：用`<style>`标签放在`<head>`里面包含css样式<br/>	2、行内样式表：标签内用style属性直接包含，适合修改简单样式<br/>	3、**外部样式表**：适合样式比较多的情况单独放在css文件<br/>

**外部样式表**：在新文件（css后缀）里直接写css属性<br/>`<head>`中加入`<link rel="stylesheet" href="css文件路径">`

