# Day6 Ajax Type Ahead

## 思考过程

1. 声明一个空数组，用于存放解析 json 后的数据

2. 运用 fetch() 发送 HTTP 请求

    - 获取返回的 Promise 对象

    - 解析 JSON 数据

    - 存入数组

3. 获取两个主要 HTML 元素（`<input>`，`<ul>`），给 `<input>` 添加事件监听（`change`, `keyup`）

4. 编写匹配输入的函数

    - 运用 `filter()` 过滤数组数据

    - 创建正则表达式，构造过滤条件

5. 编写展示匹配结果的函数

    - 获取匹配数据

    - 替换关键词放入高亮的标签

    - 构造 HTML 标签数据

    - 将匹配值的 HTML 标签放入 <ul> 中
  

## 涉及的知识点

1. Promise

   - [`fetch`](https://developer.mozilla.org/zh-CN/docs/Web/API/GlobalFetch/fetch)

2. Array

    - `push()`

    利用扩展运算符可以替代 ES5 中的 push 方法添加一个数组到另一个数组末尾，两种语法的写法如下：

    ```
    // 将arr2中的所有元素添加到arr1中

    // ES5
    var arr1 = [0, 1, 2];
    var arr2 = [3, 4, 5];
    Array.prototype.push.apply(arr1, arr2);

    // ES6
    var arr1 = [0, 1, 2];
    var arr2 = [3, 4, 5];
    arr1.push(...arr2);
    ```

3. RegExp

    - match()

    > 字符串对象的match方法对字符串进行正则匹配，返回匹配结果。

    - replace()

    > 字符串对象的replace方法可以替换匹配的值。它接受两个参数，第一个是搜索模式，第二个是替换的内容。

    - 千位分隔

    > 千分位的特征是到字符串终止位有 3n 个数字，不包括起始位

    ```
    function numberWithComas(x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
    }
    ```

    [千位分隔符的完整攻略](https://idiotwu.me/milli-formatting-digitals-with-regex/)

    [Regexp 教程](http://javascript.ruanyifeng.com/stdlib/regexp.html)

    [正则表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions)

4. [`linear-gradiend()`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/linear-gradient)
  [`perspective`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/perspective)
