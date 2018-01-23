# Dev Tools

## 给页面添加断点

在按 F12 出现的 Chrome 开发工具中，在 Elements 选项卡之中，选择页面的某个标签（以<p>标签为例），右键 → Break on → Attributes modifications。即可为该元素添加断点，当它的属性发生改变时，会自动定位到页面代码中的对应行。
此时点击页面上的p元素就可以看到效果。
通过定位到代码中相应的行就可以很方便的对页面进行调试。

## `console` 的更多用法

  - `console.log(String)` 直接将带输出的字符串传给.log()方法，就可以直接输出，这是目前最常用的调试方法，但是除了这个还有其他的方法，可以像C语言这样使用字符串的替换，如下：

    - %s： 字符串
    - %f： 浮点数
    - %o： 对象Object
    - %d： 整数
    - %c： 设定输出的样式，在之后的文字将按照第二个参数里的设置进行显示

  - `console.warn(String)` 输出警告信息，Console面板上面在文字前面显示黄色警告图标：⚠️，点击该警告消息会出现当前的程序栈的状态。

  - `console.error(String)` 输出错误信息，Console面板上面在文字前面显示红色错误图标：❌，点击该错误消息会出现当前的程序栈的状态。

  - `console.info(String)` 输出常规信息，Console面板上面在文字前面显示蓝色图标：ℹ，点击该蓝色消息会出现当前的程序栈的状态。

  - `console.clear()` 可以清空当前 Console 面板打印出的内容。还有可以通过浏览器的快捷键 Ctrl + L也可以清空Console面板，或者点击Console面板上面的灰色禁止按钮也可以直接清空Console面板。

  - `console.asset` 方法进行测试
  `console.asset(arg1,arg2)`方法接受一个表达式作为参数，如果参数返回值是 `false`，则会输出第二个参数中的内容。

  - console.table()方法，可以将数组、对象以表格的形式打印输出，如果只输出其中的某一列，可以加上第二个参数

  - `console.group()`方法中可以传入这个分组的名称。group()/groupCollapsed() 与 groupEnd() 之间的内容会自动分组，区别在于是否能自动折叠。

  - 通过`console.count()`可以对输出的对象进行计数。但需要注意的是这里的计数对象仅限于由 count() 输出的内容，并非所有 console 中的输出。

  - 用 `console.time("name")` 和 `console.timeEnd("name")` 可以分别控制开始点和结束点，它们的参数表示当前计时的名称，可以自定义但前后必须保持相同。
