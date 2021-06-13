### **<u>JS01-基本语法</u>**

弹出提示窗口`alert();`

控制台输出内容`console.log(typeof b)`

`document.write();`向html文档中写入内容

声明变量 包括各种变量类型 var 可同时声明多个变量

检查运算符 `typeof 变量名`

`Number.MAX-VALUE`数字最大值，若超过则为“无穷”（`Infinity`）,无穷可加正负，字面量即为`Infinity`

`Number.MIN-VALUE`整数中的最小值

字面量`NaN` Not a Number

Null类型只有一个值null，空对象，`typeof null`得object

Undefined值只有一个undefined 声明后未定义

强制类型转换: 通常为String Number Boolean

调用`toString()`方法 例外null和undefined没有`toString()`<br />调用`String()`函数<br />`Number()`函数 转换为数字，true转1，false转0 字符串非数字转`NaN`,空串空格转0，Null转0，undefined 转`NaN`

字符串调用`parseInt()` 或`parseFloat()`可提取字符串中得有效数字去

0x开头十六进制 0开头八进制 0b二进制

数字转布尔`Boolean()`除了`NaN`和0转换为0，其他都是true<br/>字符串转布尔除了空串其他都为true<br />undefined和null转布尔都为true

除了字符串+，其他都转换为number。可以通过-0，*1等进行类型转换<br />`+"123"` 加号表示正的，也能转数字

数字与&& ||搭配，会先转换为布尔类型再进行判断，并返回原值。&&与运算：若有两个true则返回前者，若有两个false则返回前一个false

||或运算，若第一个值为true则返回第一个值，第一个值false则返回第二个值

`NaN`不和任何值相等，包括它本身 `NaN == NaN`为false

`isNaN()`函数判断是否为NaN

`===`全等 若类型不同直接返回false

条件语句，循环语句跟c语言一样