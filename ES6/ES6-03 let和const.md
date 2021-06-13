## ES6-03 let和const

### let和var的区别

- var提前声明，全局有效 

- let不能提前声明，只能代码块内有效,同一区域不能重复声明，否则报错
  - for循环中每次都是新代码块

```js
for (let i = 0; i < 3; i++) {
  let i = 'abc';
  console.log(i);
}
// abc
// abc
// abc
```

使用do代码块可以返回{}内返回值

### const 命令

**const声明一个只读的常量。一旦声明，常量的值就不能改变。**

与let类似