# Day5 Flex Panels Image Gallery

## 涉及到的知识点：

1.[`border-box`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing)

[十个div+css布局原则与技巧](https://zhuanlan.zhihu.com/p/25855794)

>让 box-sizing 继承 div.box：

>*, *:before, *:after { box-sizing: inherit; } （存在底层样式里或某个组件、某个业务区域）

>.box{ box-sizing: border-box; } （当前需要控制的对象）


2.[`text-transform`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-transform)

> text-transform CSS属性指定如何将元素的文本大写。它可以用于使文本显示为全大写或全小写，也可单独对每一个单词进行操作。


3.[`classList`](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/classList)

4.[`flex`](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

5.[`event.propertyName`](https://developer.mozilla.org/zh-CN/docs/Web/Events/transitionend)

>`event.propertyName`: The name of the CSS property associated with the transition.

```
function toggleActive(e) {
  if (e.propertyName.includes('flex')) {
    this.classList.toggle('open-active');
  }
}

panels.forEach(panel => panel.addEventListener('transitionend', toggleActive))

```

 `transitionend` 对每一个`div`监听`transitionend`事件，当`.open`类触发的动画结束后会同时触发该事件，通过`event.propertyName`可以得到以上动画的名称，但是在Safari浏览器中，`event.propertyName === flex`，在Chrome和Firefox浏览器中，`event.propertyName === flex-grow`，因此可以通过`.includes('flex')`方法，只要属性名中包含‘flex’字符串，就继续执行。
