
| 属性      | 值      | 描述          |
| ------- | ------ | ----------- |
| colspan | number | 规定单元格可横跨的列数 |
| rowspan | number | 设置单元格可纵跨的行数 |
td 标签的其他属性在 HTML5 中已不支持，直接使用 css 即可跨列

```
<h2>表格实战 - 跨列</h2>

<table border="1" width="800">
  <caption>
    学生个人信息登记表
  </caption>
  <tr>
    <th colspan="8">高新一中初三一班学生信息登记表</th>
  </tr>
  <tr>
    <th colspan="8">学生基础信息</th>
  </tr>
  <tr>
    <td>姓名</td>
    <td>XXX</td>
    <td>国籍/地区</td>
    <td>中国</td>
    <td>姓名拼音</td>
    <td>XXX</td>
    <td>班内学号</td>
    <td>20211101</td>
  </tr>
  <tr>
    <td>性别</td>
    <td>女</td>
    <td>身份证件类型</td>
    <td>本地居民</td>
    <td>曾用名</td>
    <td>无</td>
    <td>班级</td>
    <td>初三（1）班</td>
  </tr>
  <tr>
    <td>出生日期</td>
    <td>2002年9月1日</td>
    <td>民族</td>
    <td>汉</td>
    <td>户口所在地</td>
    <td>北京</td>
    <td>入学年份</td>
    <td>2015年</td>
  </tr>
  <tr>
    <td>出生地</td>
    <td>北京</td>
    <td>政治面貌</td>
    <td>团员</td>
    <td>户口性质</td>
    <td>城镇户口</td>
    <td>入学方式</td>
    <td>普通入学</td>
  </tr>
  <tr>
    <td>籍贯</td>
    <td>海淀区</td>
    <td>健康状况</td>
    <td>良好</td>
    <td>特长</td>
    <td>书法</td>
    <td>就读方式</td>
    <td>走读</td>
  </tr>
  <tr>
    <td>身份证号</td>
    <td colspan="3"></td>
    <td>身份证有效期</td>
    <td colspan="3"></td>
  </tr>
  <tr>
    <th colspan="8">学生个人联系信息</th>
  </tr>
  <tr>
    <td>现住址</td>
    <td colspan="7"></td>
  </tr>
  <tr>
    <td>家庭地址</td>
    <td colspan="7"></td>
  </tr>
  <tr>
    <td>联系电话</td>
    <td colspan="7"></td>
  </tr>
  <tr>
    <td>电子信箱</td>
    <td colspan="7"></td>
  </tr>
</table>
```



跨行，跨列
```
<h2>表格实战 - 跨行跨列</h2>

<table border="1" width="800">
  <caption>
    版本规划任务分配表
  </caption>
  <tr>
    <th colspan="2">需求：V0.3版本规划</th>
    <th>优先级</th>
    <th>任务分解</th>
    <th>产品负责人</th>
  </tr>
  <tr>
    <td rowspan="3">功能模块1</td>
    <td>具体事项1</td>
    <td>3</td>
    <td>任务1</td>
    <td rowspan="3">@翠花</td>
  </tr>
  <tr>
    <td rowspan="2">具体事项2</td>
    <td>4</td>
    <td>任务2</td>
  </tr>
  <tr>
    <td>1</td>
    <td>任务3</td>
  </tr>
  <tr>
    <td rowspan="6">功能模块2</td>
    <td>具体事项1</td>
    <td>2</td>
    <td>任务1</td>
    <td rowspan="6"></td>
  </tr>
  <tr>
    <td rowspan="4">具体事项2</td>
    <td>3</td>
    <td>任务1</td>
  </tr>
  <tr>
    <td>2</td>
    <td>任务2</td>
  </tr>
  <tr>
    <td>1</td>
    <td>任务3</td>
  </tr>
  <tr>
    <td>4</td>
    <td>任务4</td>
  </tr>
  <tr>
    <td>具体事项3</td>
    <td>1</td>
    <td>任务1</td>
  </tr>
  <tr>
    <th colspan="5">备注信息</th>
  </tr>
  <tr>
    <td colspan="5">...</td>
  </tr>
</table>
```
