HTML 文档
HTML 文档 `描述网页`
HTML 文档 `包含 HTML 标签和纯文本`
HTML 文档也被称为`网页`
Web 浏览器的作用是读取 HTML 文档，并以网页的形式显示出它们。 浏览器不会显示 HTML 标签，而是使用标签来解释页面的内容：
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HTML标签 - Arry老师</title>
  </head>
  <body>
    <h1>我是一个标题标签</h1>

    <p>我是一个段落标签</p>
  </body>
</html>

<!--

以上代码案例解读：

<html> 与 </html> 之间的文本描述网页
<body> 与 </body> 之间的文本是可见的页面内容
<h1> 与 </h1> 之间的文本被显示为标题
<p> 与 </p> 之间的文本被显示为段落
不同的标签有不同的功能比如：p标签表示段落，h1标签表示一级标题
标签可以给文字设置不同的语义

-->
```