`<iframe>` 是 HTML 中用于在当前页面嵌入另一个 HTML 文档（如第三方内容、广告、视频等）的内联框架标签。它允许在一个网页中显示来自其他页面的内容，实现网页间的互联互通
所有主流浏览器都支持 `<iframe>` 标签
不当使用可能导致性能、安全或用户体验问题

8.1基本语法
src 属性指定要嵌入的页面 URL，可以是相对路径或绝对路径
```
<iframe src="URL"></iframe>
```

8.2常用属性

| 属性名         | 说明                                                | 示例                                            |
| ----------- | ------------------------------------------------- | --------------------------------------------- |
| width       | 设置 `<iframe>` 的宽度（像素值或百分比）。                       | `<iframe width="800"></iframe>`               |
| height      | 设置 `<iframe>` 的高度（像素值或百分比）。                       | `<iframe height="600"></iframe>`              |
| frameborder | 规定是否显示 `<iframe>` 周围的边框（HTML5 中已不推荐，建议用 CSS）。     | `<iframe frameborder="0"></iframe>`             |
| scrolling   | 规定是否在 `<iframe>` 中显示滚动条（HTML5 中已不推荐，建议用 CSS）。     | `<iframe scrolling="no"></iframe>`              |
| name        | 规定 `<iframe>` 的名称。                                | `<iframe name="myFrame"></iframe>`              |
| sandbox     | 启用对 `<iframe>` 内容的额外限制（如 `allow-same-origin`）。    | `<iframe sandbox="allow-same-origin"></iframe>` |
| allow       | 控制 `<iframe>` 内嵌页面的具体功能（如 `camera`、`microphone`）。 | `<iframe allow="camera; microphone"></iframe>`  |
| loading     | 延迟加载（`lazy`）或立即加载（默认）。                            | `<iframe loading="lazy"></iframe>`              |
| title       | 为屏幕阅读器提供描述性文本。                                    | `<iframe title="视频播放器"></iframe>`               |

8.3实践应用
嵌入网页
```
<iframe
  src="https://www.arryblog.com"
  width="800"
  height="600"
  frameborder="0"
></iframe>
```
将名为 `https://www.arryblog.com` 的网页嵌入到当前页面中，嵌入的 `<iframe>` 宽度为 800 像素，高度为 600 像素，且不显示边框

嵌入图片
```
<iframe
  src="https://sce7a2b9c9d95a-sb-qn.qiqiuyun.net/files/course/2024/08-27/2052535547fa551878.png"
  width="800"
  height="600"
  frameborder="0"
></iframe>
```
将图片嵌入到当前页面中，嵌入的 `<iframe>` 宽度为 800 像素，高度为 600 像素，且不显示边框

嵌入第三方服务
嵌入优酷视频（打开视频播放页面 -> 点击分享按钮 -> 复制代码）
```
<iframe
   height=498
   width=510
   src='https://player.youku.com/embed/XNjM2MzAzNzUyOA=='
   frameborder=0
   'allowfullscreen'></iframe>

<!-- 其中  allowfullscreen 属性为 允许全屏模式 --->
```

嵌入地图
嵌入百度地图（打开百度地图 -> 搜索具体位置 -> 点击分享 -> 复制链接地址）
```
<iframe
  src="https://j.map.baidu.com/aa/5NJ"
  width="600"
  height="450"
  style="border: 0"
  allowfullscreen=""
  loading="lazy"
  referrerpolicy="no-referrer-when-downgrade"
>
</iframe>
```
`referrerpolicy` 属性用于控制 `<iframe>` 请求资源时发送的 `Referer` 头信息。`Referer` 头信息通常用于告诉服务器请求是从哪个页面发起的。这个属性可以帮助你控制隐私和安全性，尤其是在处理敏感数据时
`no-referrer-when-downgrade` 是 `referrerpolicy` 属性的一个值，表示在以下情况下不发送 `Referer` 头信息
如果请求是从 HTTPS 页面发送到 HTTP 页面（即从安全协议降级到不安全协议），则不发送 `Referer` 头信息。
 在其他情况下（如 HTTPS 到 HTTPS 或 HTTP 到 HTTP），会发送 `Referer` 头信息。
这种策略在安全性方面提供了一种平衡。它确保在从 HTTPS 页面请求 HTTP 资源时，不会泄露来源页面的 URL，从而防止潜在的安全风险（如中间人攻击）。
在大多数情况下，这种策略是默认行为，因此通常不需要显式指定。

嵌入广告或第三方内容
```
<iframe
  src="https://huodong.taobao.com/wow/a/act/tao/dailygroup/23509/24308/wupr?spm=a21bo.jianhua/a.banner.d1.5af92a895B8bah&wh_pid=daily-565955&disableNav=YES&status_bar_transparent=true&custom_content_source=a2113w.30197676"
  width="1000"
  height="550"
  sandbox="allow-same-origin allow-scripts"
  title="广告"
>
</iframe>
```
注：
严格限制 `sandbox` 权限，防止广告代码恶意操作。
避免 `allow-popups` 防止弹窗广告。

JavaScript 控制 iframe
```
<script>
  function changeURL() {
    var iframe = document.getElementById("myFrame");
    iframe.src = "https://www.arryblog.com";
  }
</script>
<input type="button" value="改变URL" onclick="changeURL()" />
<iframe
  id="myFrame"
  src="https://www.icodingedu.com/"
  width="800"
  height="600"
  frameborder="0"
></iframe>
```

8.4iframe最佳实践

| 最佳实践                    | 说明                                   |
| ----------------------- | ------------------------------------ |
| 安全性                     |                                      |
| 设置 `sandbox`            | 限制 `<iframe>` 的权限，防止恶意代码攻击。          |
| 指定 `allow`              | 控制 `<iframe>` 内嵌页面的具体功能。             |
| 避免混合内容                  | 确保 `<iframe>` 的 `src` 使用 `https://`。 |
| 性能优化                    |                                      |
| 使用 `loading="lazy"`     | 延迟加载，减少初始页面加载时间。                     |
| 明确设置 `width` 和 `height` | 避免页面布局抖动。                            |
| 减少嵌套层级                  | 防止性能下降。                              |
| 可访问性                    |                                      |
| 添加 `title` 属性           | 为屏幕阅读器提供描述性文本。                       |
| 避免关键内容依赖 `<iframe>`     | 重要内容应直接放在主页面中。                       |
| 用户体验                    |                                      |
| 提供备用内容                  | 当 `<iframe>` 无法加载时显示备用文本或链接。         |
| 避免自动播放                  | 尤其是音频内容。                             |
| SEO优化                   |                                      |
| 避免滥用 `<iframe>`         | 搜索引擎通常无法索引 `<iframe>` 内的内容。          |
