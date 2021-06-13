## HTML笔记03基本结构标签

一、基本结构标签（骨架标签）

第一个html页面

```html
<!DOCTYPE html>
<html lang="zh-CN">
    <head>
        <meta charset="UTF-8">
        <title>第一个html网页</title>
    </head>
    <body>
        HelloWorld!
    </body>
</html>
```



| 标签            | 笔记             |
| --------------- | ---------------- |
| `<html></html>` | 最大标签，根标签 |
| `<head></head>` | 必须设置title    |
| `<body></body>` | 页面内容，元素   |



1、`<!DOCTYPE html>`

声明标签,声明为html5

2、`lang="zh-CN"`

lang缩写自language，设置语言，中文zh，英文en

3、`charset="UTF-8"`

character set 定义字符编码<br />GBK简体中文（win7）<br />BIG5繁体中文<br />UTF-8 万国码（win10）
