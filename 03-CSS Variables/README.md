# Day3   CSS Variables

## 思路：

  - 首先定义 CSS 变量，然后在页面样式中对页面变量进行关联
  - 使用 JS 实时获取变量的值，并更新 CSS 属性的值，实时改变页面的效果

## 知识点

### CSS 3

#### 1. CSS 变量

相关教程：[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Using_CSS_variables) | [CSS 变量教程](http://www.ruanyifeng.com/blog/2017/05/css-variables.html) | [深入学习 CSS 自定义属性](https://www.w3cplus.com/css3/css-properties-in-depth.html)

#### 2. [`filter`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/filter)

> CSS滤镜（filter）属提供的图形特效，像模糊，锐化或元素变色。过滤器通常被用于调整图片，背景和边界的渲染。



### JS

#### 1. [`forEach`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
> `forEach()` 方法对数组的每个元素执行一次提供的函数。

#### 2. [`dataset`](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLElement/dataset) |  [使用数据属性](https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/Using_data_attributes)

>HTMLElement.dataset属性允许无论是在读取模式和写入模式下访问在 HTML或 DOM中的元素上设置的所有自定义数据属性(data-*)集。

即：可以通过 `dataset`读取到数据
*语法*
```
string = element.dataset.camelCasedName;
element.dataset.camelCasedName = string;
```

#### 3. 监听 `mousemove`和 [`change`](https://developer.mozilla.org/zh-CN/docs/Web/Events/change) 事件

- `mousemove` 事件可以在该滑块的值变化时实时改变 CSS 全局变量
- `change` 事件是因为 `color` 的改变依赖于用户提交颜色的值

#### 4. [`document.documentElement`](https://developer.mozilla.org/en-US/docs/Web/API/Document/documentElement)

`document.documentElement`表示文档的根元素，对于HTML文档来说就是<html>
