## CSS06笔记-三大特性和盒子模型

#### 三大特性

​	一、层叠性<br  >	样式冲突时，遵循就近原则，不冲突则不层叠

​	二、继承性<br />	给父级元素的样式可以被子级元素继承

​	三、优先级<br />	排序：!important 行内样式 id选择器 类选择器 元素选择器 继承或* <br />	权重叠加：复合选择器

#### 盒子模型<br/>矩形盒子模型：边框 内边距 外边距 内容

​	边框 border

`border: border-width border-style border-color`（没有顺序）

`border-style: solid`           `border-top`

`border-collapse: collapse;` 表格细线边框

​	内边距 padding

`padding-top` `padding-left`   `padding-right `  `padding-bottom`

| padding值个数 | 含义        |
| ------------- | ----------- |
| 1             | 上左下右    |
| 2             | 上下+左右   |
| 3             | 上+左右+下  |
| 4             | 上+右+下+左 |

若盒子本身没有指定width/height属性，padding不会撑开盒子大小

​	外边距 margin

简写用法与padding相同，用于盒子之间隔开的距离<br/>`margin: 0 auto;` 把左右的外间距改成auto（盒子已经指定了width）<br/>行内元素或行内块元素设置父元素`text-align： center`

父元素外边框塌陷：与子元素的外边框合并<br/>解决：1、给父元素添加上边框。2、给父元素添加上内边距。3、给父元素添加`overflow： hidden`

消除内外边距

```css
* {
    padding: 0;
    margin: 0;
}
```

#### <u>**圆角边框（重要）**</u>

`border-radius: length;`<br />设置圆角对应的圆形半径 或占高度的百分比<br />``border-radius: 10px 20px 30px 40px;`左上开始顺时针

#### <u>**盒子阴影（重点）**</u>

`box-shadow: h-shadow v-shadow blur spread color inset`<br/>h-shadow （必须）水平阴影x轴正负  v-shadow  （必须）垂直阴影<br/>blur模糊距离 spread阴影大小 inset内阴影，不写即默认为外阴影

本子阴影

`box-shadow: h-shadow v-shadow blur color`<br/>