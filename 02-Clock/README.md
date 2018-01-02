# Day02 - Clock

## 创建页面及样式
[`box-shodow`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow)

[`transition`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transition)

[`transition` 教程](https://www.w3cplus.com/content/css3-transition)

| 值                         | 描述                              |
| -------------------------- | --------------------------------- |
| transition-property        | 规定设置过渡效果的 CSS 属性的名称 |
| transition-duration        | 规定完成过渡效果需要多少秒或毫秒 |
| transition-timing-function | 规定速度效果的速度曲线|
| transition-delay| 定义过渡效果何时开始|

[`transform`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform)

[`transform-origin`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform-origin)

>transform-origin CSS属性让你更改一个元素变形的原点。例如，rotate()的transform-origin 是旋转的中心点 (这个属性的应用原理是先用这个属性的负值translate该元素，进行变形，然后再用这个属性的值把元素translate回去)。

>没有明确定义的值会被重设回他们对应的值（Not explicitly set values are reset to their corresponding values.）

`transform-origin` 的值：

| 值               | 描述                                                            |
| ---------------- | --------------------------------------------------------------- |
| x-offset         | 定义变形中心距离和模型的左侧<length> 或<percentage> 偏移量      |
| offset-keyword   | left,right,top,bottom或 center 中之一，定义相对应的变形中心偏移 |
| y-offset         | 定义变形中心距离盒模型的顶的<length>或 <percentage> 偏移量      |
| x-offset-keyword | left，right或center中之一，定义相对应的变形中心偏移。           |
| y-offset-keyword | top，bottom或center中之一，定义相对应的变形中心偏移。           |
| z-offset| 定义变形中心距离用户视线（z=0处）的<length>（不能是<percentage>）偏移值。 |

关键字是方便的简写方法，等同于以下 `<percentage>` 值：

| keyword | value |
| ------- | ----- |
| left    | 0%    |
| center  | 50%   |
| right   | 100%  |
| top     | 0%    |
| bottom  | 100%  |