# Vue.js 学习

### Lesson 2 应用与组件实例

#### MVVM模型



```javascript
// 创建 Vue 应用
const app = Vue.createApp({
    /* 选项 */
});
// 注册全局组件
const app = Vue.createApp({});
app.component('SearchInput', SearchInputComponent);
app.directive('focus', FocusDirective);
app.use(LocalePlugin);
// 由于实例暴露时会返回同一实例，允许链式
/*
		Vue.createApp({})
  			.component('SearchInput', SearchInputComponent)
  			.directive('focus', FocusDirective)
  			.use(LocalePlugin);
*/

```

#### 根组件

**挂载**应用时被作为渲染的起点，通常被挂载到dom中，例如被挂载到`<div id="app"></div>` 则传入`#app`,`app.mount("#app");`,mount不返回应用本身，而是返回根组件实例

