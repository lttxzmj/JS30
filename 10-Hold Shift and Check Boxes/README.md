# 10 JS 实现 Checkbox 中按住 Shift 的多选功能
1. 获取所有的 <input> 元素，并添加事件监听

```
const boxs = document.querySelectorAll('.inbox input[type="checkbox"]');
boxs.forEach(box => box.addEventListener('click', handleCheck));
```

2. 编写 handleCheck 内部的处理逻辑

解决思路
在谈具体的代码时，先讲讲思路。首先来复现一下，当你按下 Shift 键进行多选时，发生了什么？

选中 A 项
按下 Shift
再选中 B 项
A-B 之间的所有项都被选中
关键点就在于 A、B 划出了一个范围，在这个范围之内的元素状态发生了改变。A 是上一次操作选中的对象，B 是此次操作对象，之后的内容将会用这两个单词来叙述。下面的方案就依据划定范围的方法不同来进行区分。

方法：
用一个变量，来标记这个范围。

变量初始值为 false，当按下 Shift 键且同时选中了某个元素的时候，遍历所有项，遍历过程中，若遇到 A 或 B，则将标记值取反。同时，将所有标记为 true 的项设置为选中。

```
let lastChecked;

function handleCheck(e) {
  //用变量 inBetween 对需要选中的元素进行标记
  let inBetween = false;
  if (e.shiftKey && this.checked) {
    checkboxes.forEach(checkbox => {
      if (checkbox === this || checkbox === lastChecked) {
        inBetween = !inBetween;
      }
      if (inBetween) {
        checkbox.checked = true;
      }
    });
  }
  //将两次点击的元素用 lastChecked 保存下来
  lastChecked = this;
}
```
