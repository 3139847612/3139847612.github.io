type 属性
无序列表有 type 属性，可以定义前导符号的样式，但在 HTML5 中已经被废弃，建议使用 CSS 替代
只作为学习和了解即可

| 属性   | 值      | 描述      |
| ---- | ------ | ------- |
| type | disc   | 默认值，实心圆 |
| type | square | 实心正方形   |
| type | circle | 空心圆     |
注意:
在 HTML 4 中的 ul 属性已废弃，HTML5 已不支持该属性，因此我们使用 CSS 代替来定义不同类型的无序列表如下：
```
<h1>无序列表标签</h1>
<p>ul的type属性在HTML5中已经废弃</p>

<h2>type="square" 实心正方形</h2>
<ul type="square">
  <li>小炒肉</li>
  <li>小龙虾</li>
  <li>剁椒鱼头</li>
  <li>酸辣白菜</li>
  <li>7分熟牛排</li>
</ul>

<h2>type="circle" 空心圆</h2>
<ul type="circle">
  <li>小炒肉</li>
  <li>小龙虾</li>
  <li>剁椒鱼头</li>
  <li>酸辣白菜</li>
  <li>7分熟牛排</li>
</ul>
```


在 HTML5 中使用 CSS 代替来定义不同类型的无序列表
```
<h1>无序列表标签</h1>
<p>ul的type属性在HTML5中已经废弃，使用CSS替代</p>

<h2>style="list-style-type:disc" 实心圆</h2>
<ul style="list-style-type:disc">
  <li>小炒肉</li>
  <li>小龙虾</li>
  <li>剁椒鱼头</li>
  <li>酸辣白菜</li>
  <li>7分熟牛排</li>
</ul>

<h2>style="list-style-type:square" 实心正方形</h2>
<ul style="list-style-type:square">
  <li>小炒肉</li>
  <li>小龙虾</li>
  <li>剁椒鱼头</li>
  <li>酸辣白菜</li>
  <li>7分熟牛排</li>
</ul>

<h2>style="list-style-type:circle" 空心圆</h2>
<ul style="list-style-type:circle">
  <li>小炒肉</li>
  <li>小龙虾</li>
  <li>剁椒鱼头</li>
  <li>酸辣白菜</li>
  <li>7分熟牛排</li>
</ul>
```