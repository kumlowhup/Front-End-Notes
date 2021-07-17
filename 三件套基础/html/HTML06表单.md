## HTML06笔记-表单

一、表单域 `<form></form>` 把表单元素信息送至服务器，包含表单元素

```html
<form action="url地址" method="提交方式" name="表单域名称">
    各种表单元素控件
</form>
```

二、`<input />`表单元素

##### 	type常用值：

	- text文本框 
	- password密码 
	- radio单选 
	- checkbook复选 
	- submit提交 
	- reset重置 
	- bottom普通按钮 
	- file文件域（上传文件）

​	**name**属性：同一name属性确保radio和checkbook，type等也需要name值配合服务器

​	checked 打勾按钮 设置值为"checked"

​	maxlength设置文本框最大值

​	value属性：按钮信息或默认显示文字

三、`<lable></label>`标签

绑定表单元素，光标点击文字或图片时自动转到相应表单值，for和id保持一致

```html
<input type="radio" id="nan"><label for="nan" name="sex">男</label>
<input type="radio" id="nv"><label for="nv" name="sex">女</label>
```

四、`<select>`下拉表单

```html
<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
    <option>选项4</option>
</select>
```

默认选定属性selected = "selected"

五、`<textarea></textarea>`文本域