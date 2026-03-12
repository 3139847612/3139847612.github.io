定义和用法
`<!DOCTYPE>` 声明必须是 HTML 文档的第一行，位于 `<html>` 标签之前。`
 `<!DOCTYPE>` 声明不是 HTML 标签，它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。
 在 HTML 4.01 中，`<!DOCTYPE>` 声明引用 DTD，因为 HTML 4.01 基于 SGML。DTD 规定了标记语言的规则，这样浏览器才能正确地呈现内容。

SGML（Standard Generalized Markup Language
即标准通用标记语言) SGML 是国际上定义电子文档和内容描述的标准。
HTML5 不基于 SGML，所以不需要引用 DTD

提示：
请始终向 HTML 文档添加 `<!DOCTYPE>` 声明，这样浏览器才能获知文档类型。
不写 DTD 会引发浏览器的一些兼容问题
不同版本的 HTML 有不同的 DTD 写法

HTML 4.01 与 HTML5 之间的差异
在 HTML 4.01 中有三种 <!DOCTYPE> 声明。
在 HTML5 中只有一种


HTML5 标准
```
<!DOCTYPE html>

<!DOCTYPE > 声明没有结束标签。
<!DOCTYPE > 声明对大小写不敏感，以下任意方式都可以。但，建议使用 <!DOCTYPE html>

<!DOCTYPE html>
<!DOCTYPE html>
<!DOCTYPE html>
<!DOCTYPE html>
```

HTML4.01 严格版
```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```

HTML4.01 过渡版
```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```
HTML4.01 框架版
```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
```
