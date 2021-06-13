## HTML05笔记-表格和列表

#### 一、基本语法

```html
<table>
    <tr>
        <th>表头1</td>
        <th>表头2</td>
    </tr>
    <tr>
        <td>表格1</td>
        <td>表格2</td>
	</tr>
</table>
```

table 定义表格标签 th表头 tr行 td单元格

#### 二、结构标签

`<thead></thead>`  整个表头区域

 `<tbody></tbody>`整个表格主体区域

#### 三、合并单元格

`<colspan>` 跨列单元格

`<rowspan>`跨行单元格

方法：

1、将目标单元格的td标签中加入属性colspan或rowspan

2、colspan或rowspan的值为合并单元格个数

3、把被合并的单元格的td标签删除

#### 四、<u>**列表**</u>

1、无序列表

```html
<ul>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
</ul>
```

`<ul></ul>`无序列表只能嵌套`<li></li>`

`<li></li>`能容纳各种元素

`list-style: none;` 取消列表小圆点

2、有序列表

```html
<ol>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
</ol>
```

`<ol></ol>` 有序列表

3、<u>自定义列表</u>

```html
<dl>
    <dt>名词一</dt>
    <dd>名词一解释</dd>
    <dd>名词一解释</dd>
</dl>
```



`list-style: none;` 取消列表小圆点