# Day4 Array Cardio Day 1

## TaskList

网站给出了一个inventors数组，包含了名、姓、出生日期和死亡日期；以及people数组，包含一组人名，名和姓中间以逗号分隔。在此基础上完成以下练习。

1.

Q: 筛选出出生在16世纪（1500-1599年）的发明家。

A: [`Array.prototype.filter()`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

> filter() 方法创建一个新数组, 其包含通过所提供函数实现的测试的所有元素。

```
const filteen = inventors.filter((inventor) => inventor.year >= 1500 && inventor.year <= 1600);
```

2.

Q: 列出发明家的名和姓的数组。

A: [`Array.prototype.map()`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

>`map()` 方法创建一个新数组，其结果是该数组中的每个元素都调用一个提供的函数后返回的结果。

[模版字符串](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/template_strings)

```
const inventorName = inventors.map((inventor) => `${inventor.first} ${inventor.last}`);
```

3.

Q: 根据发明家的出生日期，按照从大到小的顺序进行排序。
A:
[`Array.prototype.sort()`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)

```
const ordered = inventors.sort(
  (a, b) => a.year > b.year
    ? 1
    : -1
);
```
4.

Q: 所有的发明家一共活了多少岁。

A:[`Array.prototype.reduce()`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

```
const liveYear = inventors.reduce((total, inventor) => {
  return total + (inventor.passed - inventor.year)
}, 0)
```

5.

Q: 按照发明家的年龄大小排序

A:

```
const oldest = inventors.sort(function (a, b) {
  const lastInventor = a.passed - a.year;
  const nextInventor = b.passed - b.year;
  return lastInventor > nextInventor
    ? -1
    : 1;
});
```

6.

Q: 列出巴黎所有名字中包含'de'的路名。在以下网站提供的信息来做。（https://en.wikipedia.org/wiki/Category:Boulevards_in_Paris）

A:
[`Array.from()`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/from)

>`Array.from()` 方法从一个类似数组或可迭代对象中创建一个新的数组实例。

7.

Q: 按照字母表的顺序，将人们的姓氏进行排序。

A: [`split`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/split)
```
const lastNameArray = people.sort((a, b) => {
  const [aFirst, aLast] = a.split(', ');
  console.log(a.split(', '));
  const [bFirst, bLast] = b.split(', ');
  return aLast > bLast
    ? 1
    : -1;
});
```

8.

Q: 分别计算出包含每一个种类的个数。

A: [`in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/in)

>如果指定的属性在指定的对象或其原型链中，则in 运算符返回true。


```
var transportation = data.reduce(function (obj, item) {
  if (item in obj) {
    obj[item]++;
  } else {
    obj[item] = 1;
  }
  return obj;
}, {});
```

或者：
```
const transportation = data.reduce(function(obj, item) {
  if (!obj[item]) {
    obj[item] = 0;
  }
  obj[item]++;
  return obj;
}, {});
```

很好的参考资料：

[Array Map, Filter and Reduce in JS](https://atendesigngroup.com/blog/array-map-filter-and-reduce-js)

[Javascript Array中的filter、map和reduce(中文翻译版)](http://zerosoul.github.io/2016/12/06/array-filter-map-reduce-in-js/)
