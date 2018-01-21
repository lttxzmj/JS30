# Array Cardio Day 2

## 知识点
  - 扩展运算符

    >扩展运算符（spread）是三个点（...）。它好比 rest 参数的逆运算，将一个数组转为用逗号分隔的参数序列。

    [扩展运算符](http://es6.ruanyifeng.com/#docs/array)

  - `find()` `findIndex()`

    [教程](http://es6.ruanyifeng.com/#docs/array#%E6%95%B0%E7%BB%84%E5%AE%9E%E4%BE%8B%E7%9A%84-find-%E5%92%8C-findIndex)

  - `Array.prototype.some()`
    >.some(callback)函数测试数组中的每一项是否满足传入函数，只要有一项满足就返回true，否则返回false。 回调函数有三个参数，分别为currentValue，index，array,分别代表待传入的值，当前元素在数组中的下标，传入的数组。

  - `Array.prototype.every()`
    >.every(callback)函数测试数组中的每一项是否满足传入函数，只有所有的项都满足才返回true，否则返回false。 回调函数有三个参数，分别为currentValue，index，array,分别代表待传入的值，当前元素在数组中的下标，传入的数组。

  - `Array.prototype.splice()`
    > .splice()方法，是一个十分强大的方法，既可以删除一个数组中的若干项，也可以向数组中某个位置添加若干项，语法如下array.splice(start, [deleteCount], [item1, item2, ...]),start代表从什么位置开始改变这个数组，从0开始索引；deleteCount代表要删除的个数，可选的；[item1, item2, ...]代表向数组中添加的元素；若deleteCount=0,又有[item1, item2, ...]存在，就可以实现在指定位置添加元素的效果；如果deleteCount=(some number)，且无[item1, item2, ...]，就可以从数组中删除若干个元素。但是此方法是对原数组进行改变，经过.splice()方法处理后，原数组回丢失，因此再采用以下方法实现删除操作，而不损坏原数组。

    ```
    comments.splice(findCommentIndex,1);

    const newComments = [
      ...comments.slice(0,findCommentIndex),
      ...comments.slice(findCommentIndex+1)
    ];
    ```

    [文档](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
