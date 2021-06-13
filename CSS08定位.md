## CSS08定位

1、静态定位static

2、相对定位 **<u>relative</u>**

以自己原有的位置作为参考系进行定位

3、绝对定位**<u>absolute</u>**

**以最近一级且有定位属性的元素**的top bottom left right定位，不超出上级元素范围(子绝父相)<br />**脱标，不占有原有位置**

定位语法

```css
div {
    position: absolute||relative;
    top: 20px;
    left: 30px;
}
```

**<u>4、固定定位</u>**

固定于浏览器可视区

`position: fixed;`

与父元素没有任何关系，不占有原有位置

sticky 占有原先位置

5、z-index

控制盒子前后层叠顺序，可为正、负、0，当属性值相同时，后来居上

定位特殊属性：行内元素加absolute或fixed，可以直接设置高度宽度，块元素不给高宽，默认大小是内容大小。脱标，不会外边塌陷。