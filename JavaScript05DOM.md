JavaScript05DOM

DOM: 文档对象模型（Document Object Model）

文档-网页 对象-节点 模型-体现对象之间的关系

节点（node）

文档节点 元素结点 属性节点 文本节点

浏览器已经提供了文档节点对象，这是对象是window属性，可以在页面中直接使用，文档节点代表整个网页 document 对象 `HTMLDocument `

通过id获取一个对象 `document.getElementById("idName")`



绑定事件

`objName.eventName = function(){}` 例如`btn.onclick = function(){ alert("1234");}`

onload事件在页面完成后触发 若在head中写代码则放在`window.onload`的函数中，确保页面加载完之后再执行

`document.getElement是ByTagName("tagName")`通过标签名获取**一组**对象，返回值为类数组

`document.getElementsByName("name")`通过name属性**一组**节点对象，返回值为类数组

`objName.innerHTML`获取元素中html代码 读取和修改其中的内容

`objName.propertyName`获取对应的属性，读取class时用className属性

`objName.childNodes`  获取包括文本节点在内的所有子节点

`objName.firstChild`第一个子节点 lastChild 最后一个子节点

`objName.children` 获取子元素

`objName.firstChild` 获取第一个子元素（不支持ie8）lastChild

`parentNode`获取父节点

`previousSibling` 当前节点前一个兄弟节点

`nextSibling`当前节点的后一个兄弟节点

`innerText`获取元素内部的文本内容



DOM增删改

`appendChild();`把新节点添加到子节点

`removeChild()；`删除节点

`createElement();`创建元素节点，传入新添加标签的标签名字符串

`createTextNode();`创建一个文本节点，传入文本内容名

`父节点.insertBefore(新节点，旧节点);`在指定的子节点前面插入新的子节点 

`父节点.replaceChild(新节点，旧节点); `使用指定节点替换旧节点

`父节点.remove(子节点)` 移除节点

`confirm();`显示一段带有确认和取消的对话框，点击确认返回值为true，点击取消返回值为false



读取样式

元素.style.样式名 读取**内联样式**（无法读取样式表中的样式），可以通过直接赋值修改内联样式

为了兼容IE8的读取当前样式的方法（这里的name为样式名）

```js
function getStyle(obj, name){
    if(window.getComputedStyle){
        //正常浏览器
        return getComputedStyle(obj ,null)[name];
    }else{
        //兼容IE8
        return obj.currentStyle[name];
    }
}
```

clientWeight clientHeight 获取元素的可见高度和宽度（不带px，可以直接计算）

offsetLeft 当前元素相对于定位父元素的水平偏移量

offsetTop 当前元素相对于定位父元素的垂直偏移量

scrollWidth scrollHeight 可以获取元素整个滚动区域的宽度和高度

scrollLeft 可以获取水平滚动条滚动的距离

scrollTop 可以获取垂直滚动条滚动的距离

当scrollHeight - scrollTop == clientHeight 垂直滚动条滚到底了

当scrollWidth - scrollLeft == clientWidth 水平滚动条滚到底了