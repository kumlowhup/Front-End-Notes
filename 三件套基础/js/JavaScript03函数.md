### JavaScript03函数

函数：封装代码块的对象 `var fun = new Function();`

可以在构造函数中传入字符串形式的代码块,但是很少使用

利用函数声明创建函数

```js
function fun(/*形式参数列表*/){
    //代码语句
}
```

创建匿名函数

```js
var fun = function(){
    //代码
}
```

接受返回值

`console.log(函数名)；`打印函数的代码

不加括号不会调用函数

`console.log(函数名())；`打印函数的返回值

枚举对象中的变量



```js
for(var n in obj){
    console.log(n);//遍历属性名
    console.log(obj[n]);//便利属性值
}
```

全局作用域：

`window`浏览器变量 直接调用函数时`window`作为`this`传给函数，则函数调用永远为window，若使用调用对象的方法的方式，`this`为对象

构造函数执行流程：

`var per = new Person();`

​	1、立即创建一个新的对象

​	2、将新建的对象设置为函数中的this

​	3、执行函数中的代码

​	4、把新建的对象返回

创建函数时，解析器会向函数中添加一个属性prototype，当new调用构造函数时，会在新创建的对象中添加隐藏`__proto__`属性，跟构造函数中的prototype属性值相同（指向同一个原型对象）

调用对象属性时若找不到，会在他的原型对象中寻找

如果用in检查对象中是否含有某个属性时，如果对象中没有，原型中有，同样会返回true,可以使用`hasOwnProperty()`方法检查对象自身是否有对应属性

`hasOwnProperty()`在Object对象（构造对象的原型）的原型中。若在Object中依然没有找到，则返回undefined

`toString()`方法在原型的原型中