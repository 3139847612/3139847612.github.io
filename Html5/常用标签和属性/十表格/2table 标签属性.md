
| 属性          | 描述                       |
| ----------- | ------------------------ |
| `border`      | 表格的边框                    |
| `width`       | 表格的宽度（HTML5 不支持）         |
| `cellpadding` | 单元边沿与其内容之间的空白（HTML5 不支持） |
| `cellspacing` | 单元格之间的空白（HTML5 不支持）      |
在 HTML5 中 table 标签的大部分属性`已经废弃`，全部用 CSS 代替了。

```
<h1>table标签</h1>

<table border="1" width="500" cellpadding="10" cellspacing="0">
  <!-- caption标签，表格标题 -->
  <caption>
    同学通讯录
  </caption>
  <tr>
    <!-- th，表头 -->
    <th>姓名</th>
    <th>性别</th>
    <th>年龄</th>
    <th>所在城市</th>
  </tr>
  <tr>
    <td>arry</td>
    <td>男</td>
    <td>18</td>
    <td>北京</td>
  </tr>
  <tr>
    <td>豆豆</td>
    <td>女</td>
    <td>21</td>
    <td>上海</td>
  </tr>
  <tr>
    <td>翠花</td>
    <td>19</td>
    <td>男</td>
    <td>深圳</td>
  </tr>
</table>
```

