对文本内容进行格式化处理的相关标签

1.1span 标签
`<span>`标签是文本中的`区块标签`，没有任何显示的效果，可以结合 css 来定位区块的样式
需要被特殊标记的元素也会使用 span 标签
```
<h1>语义化标签</h1>

<h2>span 标签</h2>

<p>
  商品价格：
  <span>368</span>元，优惠价：<span>298</span>元
</p>
```

1.2文本格式化标签

| 标签             | 功能                     | 示例                                                                                      | 语义化用途                                                                                               |
| -------------- | ---------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `<strong>`     | 定义加重语气，表示特别重要的文字（粗体显示） | `<p>这是<strong>重要</strong>内容</p>`                                                          | 表示文本内容的重要性和紧迫性                                                                                      |
| `<em>`         | 强调文本（斜体显示）             | `<p>这是<em>强调</em>内容</p>`                                                                  | 表示文本内容的语气或情感强调                                                                                      |
| `<mark>`       | 高亮文本                   | `<p>这是<mark>高亮</mark>内容</p>`                                                              | 标记需要用户特别注意的文本                                                                                       |
| `<del>`        | 删除线文本                  | `<p>原价<del>100元</del></p>`                                                                | 表示已删除或不再准确的内容                                                                                       |
| `<ins>`        | 下划线文本（插入内容）            | `<p>现价<ins>80元</ins></p>`                                                                 | 表示新增或修改的内容                                                                                          |
| `<u>`          | 下划线文本（非强调用途）已被 CSS 替代  | `<p><u>拼写错误</u></p>`                                                                      | 不推荐用于强调，建议用 CSS 或语义标签                                                                               |
| `<small>`      | 小号字体文本                 | `<p><small>版权声明</small></p>`                                                              | 表示次要文本（如版权、免责声明）                                                                                    |
| `<sup>`        | 定义上标字                  | `H<sub>2</sub>O 或 2<sup>2</sup>`                                                      | 用于科学公式、脚注等                                                                                          |
| `<sub>`        | 定义下标字                  | `H<sub>2</sub>O 或 2<sup>2</sup>`                                                      | 用于化学式、数学公式等                                                                                         |
| `<pre>`        | 预格式化文本                 | `<pre>保留空格和换行</pre>`                                                                      | 用于显示代码、诗歌等需要保留格式的内容定义预格式文本。 被包围在 pre 标签 元素中的文本通常会保留空格和换行符。而文本也会呈现为等宽字体。 pre 标签的一个常见应用就是用来表示计算机的源代码。 |
| `<code>`       | 计算机代码片段                | `<p>使用<code>console.log()</code></p>`                                                     | 标记代码片段                                                                                              |
| `<kbd>`        | 键盘输入文本                 | `<p>按<kbd>Ctrl+S</kbd>保存</p>`                                                             | 表示用户键盘输入的内容                                                                                         |
| `<samp>`       | 程序输出样本                 | `<p>输出结果：<samp>Hello</samp></p>`                                                          | 表示程序或系统的输出内容                                                                                        |
| `<var>`        | 变量名                    | `<p>定义变量：<var>x</var>=10</p>`                                                             | 用于数学表达式或编程文档中的变量                                                                                    |
| `<abbr>`       | 缩写词                    | `<p><abbr title="World Wide Web">WWW</abbr></p>`                                          | 表示缩写词，可通过`title`提供全称                                                                                |
| `<q>`          | 短引用                    | `<p>他说：<q>你好</q></p>`                                                                     | 表示短引用，浏览器可能自动加引号                                                                                    |
| `<blockquote>` | 长引用                    | `<blockquote>长引用内容</blockquote>`                                                          | 表示长引用，通常缩进显示                                                                                        |
| `<cite>`       | 引用来源                   | `<p>出自《<cite>书名</cite>》</p>`                                                              | 表示作品标题（如书籍、电影等）                                                                                     |
| `<dfn>`        | 定义术语                   | `<p><dfn>HTML</dfn>是标记语言</p>`                                                             | 表示术语的定义                                                                                             |
| `<b>`          | 觉加粗（无语义）已被 CSS 替代      | `<p><b>粗体文本</b></p>`                                                                      | 仅用于视觉样式，无语义                                                                                         |
| `<i>`          | 视觉斜体（无语义）已被 CSS 替代     | `<p><i>斜体文本</i></p>`                                                                      | 仅用于视觉样式，无语义                                                                                         |
| `<figure>`     | 一段独立的内容                | `<figure><img src="images/6.webp" alt="" /><figcaption>小米智能家居，智能门锁</figcaption></figure>` | 代表一段独立的内容，与说明 figcaption 标签配合使用。figure 标签规定独立的流内容（图像、图表、照片、代码等等）。                                   |
| `<figcaption>` | 一个独立的引用单元              | `<figure><img src="images/6.webp" alt="" /><figcaption>小米智能家居，智能门锁</figcaption></figure>` | 标签为`<figure>` 元素定义标题                                                                                |
| `<time>`       | 日期和时间                  | `<p>会议将于 <time datetime="2028-06-15T14:30">6月15日下午2:30</time> 开始。</p>`                    | 包含 `datetime` 属性提供机器可读格式                                                                            |

代码样例：
```
<h1>语义化标签</h1>

<h2>span 标签</h2>
<p>
  商品价格：
  <span>368</span>元，优惠价：<span>298</span>元
</p>

<h2>文本格式化标签</h2>
b标签：<b>定义粗体文本</b> <br /><br />
em标签：<em>表示被强调的文本</em> <br /><br />
i标签：<i>斜体</i> <br /><br />
u标签：<u>定义文本下划线</u> <br /><br />
strong标签：<strong>定义加重语气，表示特别重要的文字</strong><br /><br />
del标签：<del>定义删除字 </del><br /><br />
mark标签：<mark>一段需要被高亮的文本</mark>

<h3>sub 标签</h3>
<p>碳在氧气中充分燃烧：C + O<sub>2</sub> = CO<sub>2</sub></p>
<p>铁在氧气中燃烧： 3Fe + 2O<sub>2</sub> = Fe<sub>3</sub>O<sub>4</sub></p>

<h3>sup 标签</h3>
<p>2<sup>3</sup> + 3<sup>2</sup> = 17</p>

<h3>pre 预格式化文本</h3>
<pre>
  预格式化文本

  被包围在 pre标签 元素中的文本通常会保留空格和换行符。而文本也会呈现为等宽字体

  pre 标签的一个常见应用就是用来表示计算机的源代码。

  &lt;div id="app"&gt;
      &lt;button @click="count++"&gt;
        Count is: {{ count }}
      &lt;/button&gt;
  &lt;/div&gt;

</pre>

<h3>figure、figcaption 标签</h3>
<p>
  代表一段独立的内容，与figcaption配合使用。figure
  标签规定独立的流内容（图像、图表、照片、代码等等）。一个独立的引用单元，标签为figure
  元素定义标题
</p>
<p>
  <figure>
    <img src="images/6.webp" alt="" />
    <figcaption>小米智能家居，智能门锁</figcaption>
  </figure>

  <figure>
    <img src="images/7.webp" alt="" />
    <figcaption>小米智能家居，平衡车</figcaption>
  </figure>
</p>

<h3>blockquote 和 q</h3>

<blockquote cite="https://example.com/quote">
  <p>设计不仅仅是外观和感觉，设计是产品如何工作。</p>
  <footer>— Steve Jobs</footer>
</blockquote>

<p>正如 <q>时间就是金钱</q> 这句话所说...</p>

<h3>time 标签</h3>

<p>会议将于 <time datetime="2028-06-15T14:30">6月15日下午2:30</time> 开始。</p>
```

