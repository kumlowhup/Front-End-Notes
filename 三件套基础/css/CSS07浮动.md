## CSS07-浮动

标准流：便签按规定好的默认方式排列

布局准则：**多个块级元素纵向排列找<u>标准流</u>，多个块级元素横向排列找<u>浮动</u>**

float属性用于创建浮动框，将其移动到一边，直到左边缘或右边缘触及包含块或另一个浮动框的边缘

`float: 属性值;` none（默认） left right

<u>**浮动特性（重难点）**</u>

1、脱离标准流的控制（浮）移动到指定位置（动），（俗称**浮标**）<br/>2、浮动的盒子不再保留原来的位置（<u>浮动的盒子可盖在后面的标准流盒子的上方，但是不会压住之前的标准流盒子</u>）<br/>3、浮动盒子会一行内显示，上缘对齐<br/>4、浮动元素具有行内块元素特性，行内元素浮动后无需设置高度宽度

<u>**清除浮动**</u>元素脱离标准造成的影响<br />1、`clear: both;` 额外标签法，末尾添加一个新的空白**块元素**，把clear属性作用到空白块元素上<br />2、`overflow: hidden;` （外边框合并也用它）<br />3、after伪元素法

```css
.clearfix:after{/*伪元素是行内元素 正常浏览器清除浮动方法*/
        content: "";
        display: block;
        height: 0;
        clear:both;
        visibility: hidden;
    }
    .clearfix{
        *zoom: 1;/*为了迁就旧版浏览器*/
    }
```

4、双伪元素

```css
.clearfix:before,
.clearfix:after {
content: "";
display: table;
}
.clearfix:after {
clear: both;
}
/* ie6 7 专门清除浮动的样式*/
.clearfix {
*zoom:1;
}
```

