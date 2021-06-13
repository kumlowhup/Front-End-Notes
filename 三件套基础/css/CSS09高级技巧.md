## CSS09高级技巧

1、三角形

将使用border

```css
div {
    width: 0;
    height: 0;
    left: 500px;
    top: 200px;
    border: 50px solid transparent;
    border-top-color: blue;
    border-top-width: 86.6px;
    border-bottom-width: 13.4px;
}
```

将盒子高度和宽度设为0，设置大值的边框，将挤成三角形，也可以设置

2、表单轮廓线outline和防止表单域拖拽

`input { outline: none };`取消表单轮廓线

`textarea { resize: none };防止表单域拖拽`

3、图片底部默认空白缝隙

行内块元素默认与文字的基线对齐。

`text-align: bottom || middle ||top;`垂直居中

`display: block;`

4、溢出文字省略号显示

```css
div{
    /*先强制一行内显示文本,默认是normal自动换行*/
    white-space: nowrap;
    /*超出的部分隐藏*/
    overflow: hidden;
    /*文字用省略号替代超出的部分*/
    text-overflow: ellipsis;
}
```

​	多行文字显示省略号 (适合webkit 移动端浏览器)

```css
div {
    overflow: hidden;
    text-overflow: ellipsis;
    /*弹性伸缩盒子模型显示*/
    display: -webkit-box;
    /*限制在一个块元素显示的文本的行数*/
    -webkit-line-clamp: 2;
    /*设置或检索伸缩盒子对象的子元素排列方式*/
    -webkit-box-orient: vertical;
}
```

5、布局技巧：

margin负值：取消紧贴时盒子两边框问题

文字不会被浮动的盒子覆盖，可以用浮动使文字环绕盒子