meta 标签及属性的含义
```
<!--IE8及以上的版本按照最新的标准去渲染-->
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
```

`X-UA-Compatible` 是什么？
X-UA-Compatible 是 IE8 的一个专有`<meta>`属性，它告诉 IE8 采用何种 IE 版本去渲染网页，在 html 的`<head>`标签中使用，IE8 以下版本不识别
Edge 模式告诉 IE 以最高级模式渲染文档，也就是任何 IE 版本都以当前版本所支持的最高级标准模式渲染，避免版本升级造成的影响。
简单的说，就是什么版本 IE 就用什么版本的标准模式渲染。

最佳的兼容模式方案：
```
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
```
添加”chrome=1“ 将允许站点在使用了谷歌浏览器内嵌框架（Chrome Frame）的客户端渲染，对于没有使用的，则没有任何影响。
百度目前也是使用该模式

`viewport`主要用作移动端适配
width：用来设置 layout viewport 的宽度
device-width ：设置成设备的实际宽度
initial-scale=1.0 ：防止浏览器对页面进行缩放 1:1 显示，即不缩放
```
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

完整解读
```
<!--声明当前文档类型为 html5标准-->
<!DOCTYPE html>
<!--声明当前页面的语言类型-->
<html lang="en">
  <head>
    <!--网页的编码集-->
    <meta charset="UTF-8" />
    <!--IE8及以上的版本按照最新的标准去渲染-->
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <!--用户移动端适配-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!--网页标题-->
    <title>艾编程</title>
    <!--网页关键词-->
    <meta name="Keywords" content="艾编程,WEB前端,Java架构师,Python课程" />
    <!--网页描述-->
    <meta name="description" content="为每个互联网人提供高质量的终身学习平台" />
  </head>
  <body></body>
</html>
```
