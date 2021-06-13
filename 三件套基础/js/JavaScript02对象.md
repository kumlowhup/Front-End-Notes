### JS02对象

一、

​	1、内建对象

​		ES标准中定义的对象，再任何的ES实现中都可以使用<br />		例如：Math String Number Boolean Function Object

​	2、宿主对象（浏览器对象）

​		例如：DOM BOM

​	3、自定义对象

二、创建对象

​	`var obj = new Object();`或`var obj = {};`（默认为Object）

​	构造函数类似java

​	`对象.属性名` 直接添加新属性,对象的属性名不强制要求标识符规范。

特殊属性名 `obj[属性名]` 中括号中可以放变量名 属性值可以是任意的数据类型，甚至可以是对象

检查属性是否在对象中 `属性名 in 对象`

三、call和apply

可以将对象指定为第一个参数，此时对象会成为函数执行时的this

call方法可以将实参在对象后依次传递给形参，apply则需要封装好数组统一传递

`funName.call(obj,a,b); `	`funName.apply(obj,[a,b]);`

arguements类数组对象，封装实参的对象，arguements.callee对应函数对象