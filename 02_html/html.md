# HTML

> 本笔记是主要参考w3schools

## HTML 简介

---

### 什么是HTML?

HTML是用于创建网页的标准标记语言

- HTML 代表超文本标记语言
- HTML 描述了使用标记语言的网页结构
- HTML 元素是HTML页面的构件块
- HTML 元素由标记表示
- HTML 标记内容
- 浏览器不现实HTML标记, 但使用它们来呈现页面内容

---

### HTML 标签

HTML标记是由尖括号括起来的元素名称

---

### Web Browsers

Web浏览器读取HTML文档并显示它们, 浏览器不显示HTML标记, 但使用它们来确定如何显示文档

---

### `<!DOCTYPE>` 声明

 `<!DOCTYPE>` 声明表示文档类型, 并帮助浏览器能够正确显示网页

它必须只在页面顶部出现一次

`<!DOCTYPE>` 不分大小写

 `<!DOCTYPE>` HTML5声明是:

```html
<!DOCTYPE html>
```

---

## HTML 元素

### HTML 元素

HTML元素通常由开始标记和结束标记组成, 其中插入内容

---

### 嵌套的HTML元素

HTML元素可以嵌套 (元素可以包含元素)

所有HTML文档都包含嵌套的HTML元素

---

## HTML 属性

- 所有HTML元素都可以具有属性
- 属性提供有关元素的其他信息
- 始终在开始标记中指定属性
- 属性通常以名称/值对的形式处出现, 如 name = "value"

---

### href属性

HTML链接使用`<a>`标记定义, 链接地址在`href`属性中指定

```html
<a href="https://www.w3schools.com">This is a link</a>
```

---

### src属性

HTML图像使用`<img>`标记定义

图像源文件名在`src`属性中指定

```html
<img src="img_girl.jpg">
```

---

### 宽度和高度属性

HTML中的图像具有一组大小属性, 用于指定图像的宽度和高度, 指定一个就按比例缩放

```html
<img src="img_girl.jpg" width="500" height="600">
```

---

### alt属性

`alt`当无法显示图像的时候, 该属性指定要使用的替代文本, 也可以供屏幕阅读器阅读

---

### 样式属性

`style`属性用于指定元素的样式, 如颜色, 字体, 大小等.

```html
<p style="color:red">I am a paragraph</p>
```

---

### lang属性

`lang`属性可以在`<html>`标记中声明文档的语言

语言是用`lang`属性声明的

```html
<!DOCTYPE html>
<html lang="en-US">
<body>

...

</body>
</html>
```

前两个字母是指定语言(en), 如果有方言, 请再使用两个字母(US)

---

### 标题属性

`title`属性被添加到`<p>`元素中, 或者其他元素中, 将鼠标悬停在元素上, title属性的值将以工具提示的方式显现.

---

### 属性使用小写

HTML5标准没有规定大小写, W3C建议使用小写

---

### 属性值用引号包裹

有时候包含空格的属性值如果没有引号就会报错, 一般都使用双引号

---

## HTML 标题

使用 `<h1>` 到 `<h6>` 标签定义标题

> 注意: 浏览器会在标题前后自动添加一些空格(边距)

---

### 标题的重要性

搜索引擎使用标题来索引网页的结构和内容

用户按标题浏览页面, 使用标题显示文档结构很重要

不要仅仅用标题标签来加粗和加大

---

### 更大的标题

每个HTML标题都有一个默认的大小, 但是, 你可以使用`style`中的`font-size`属性来指定具有该属性的任何标题的大小

---

### HTML水平线

`<hr>` 标签定义HTML的分割线, 用于分割页面中内容

---

### <head> 元素

HTML中的 `<head>` 元素与HTML标题无关, 它是元数据的容器.

元数据是有关HTML文档的数据, 浏览器是不显示元数据

---

## HTML 段落

`<p>` 元素定义了一个段落

```html
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

> 注意: 浏览器会在段落前后自动添加一些空格(边距), 并且会删除额外的空格和空行

---

### 不要忘记结束标签

虽然不写结束标签, 大多数浏览器也会正确解析, 但是不建议这样做, 容易导致意外结果和错误.

---

### HTML换行符

`<br>` 元素定义换行符, 它是一个空标签, 没有结束标记

---

### HTML `<pre>` 预格式化文本

HTML的 `<pre>`元素定义了预格式化的文本, 以固定宽度字体显示, 并保留空格和换行符

```html
<pre>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>
```

---

## HTML 样式

使用`style`属性设置HTML元素的样式. 其语法是:

```html
<tagname style="property:value;">
```

- `background-color`属性定义HTML元素的背景颜色
- `color`属性定义HTML元素的文本颜色
- `font-family`属性定义了用于HTML元素的字体
- `font-size`属性定义了HTML元素的文本大小
- `text-align`属性定义了HTML元素的水平文本对齐方式

---

##  HTML 文本格式

- `<b>` - 加粗文字
- `<strong>` - 重要文字
- `<i>` - 斜体文字
- `<em>` - 强调文本
- `<mark>` - 标记文字
- `<small>` - 小文字
- `<del>` - 删除线文字
- `<ins>` - 插入的文字
- `<sub>` - 下标文字
- `<sup>` - 上标文字

---

##  HTML 引文和引文元素

### HTML `<q>` 用于短引用

HTML `<q>` 元素定义了一个简短的引用, 浏览器通常在 `<q>` 元素周围插入引号

```html
<p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
```

### `<blockquote>` 源引用块

HTML `<blockquote>` 元素定义了从另一个源引用的部分, 浏览器通常会缩进这个元素

```html
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 50 years, WWF has been protecting the future of nature.
The world's leading conservation organization,
WWF works in 100 countries and is supported by
1.2 million members in the United States and
close to 5 million globally.
</blockquote>
```

---

### HTML `<abbr>` 表示缩写

HTML `<abbr>` 元素定义缩写或首字母缩略词, 它可以为浏览器, 翻译系统和搜索引擎提供有用的信息.

```html
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

---

### HTML `<address>` 联系信息

HTML `<address>` 元素定义文档或文章的联系信息 (作者/所有者), 它通常被显示为斜体, 大多数浏览器会在元素之前和之后添加换行符.

```html
<address>
Written by John Doe.<br> 
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
```

---

## HTML 块和内联元素

每个HTML元素都有一个默认的显示值, 具体取决于它的元素类型, 大多数元素的默认显示值是块或内联

---

### 块级元素

块级元素始终在新行上开始并占用可用的全宽(尽可能向左和向右延伸)

```html
<div>Hello</div>
<div>World</div>
```

HTML中的块级元素有


`<address>` `<article>` `<aside>` `<blockquote>` `<canvas>` `<dd>` `<div>` `<dl>` `<dt>` `<fieldset>` `<figcaption>` `<figure>` `<footer>` `<form>` `<h1>`-`<h6>` `<header>` `<hr>` `<li>` `<main>` `<nav>` `<noscript>` `<ol>` `<output>` `<p>` `<pre>` `<section>` `<table>` `<tfoot>` `<ul>` `<video>`

---

### 内联元素

内联元素不会在新行上启动, 只会占用所需的宽度

```html
<span>Hello</span>
<span>World</span>
```

HTML中的内联元素有:

`<a>` `<abbr>` `<acronym>` `<b>` `<bdo>` `<big>` `<br>` `<button>` `<cite>` `<code>` `<dfn>` `<em>` `<i>` `<img>` `<input>` `<kbd>` `<label>` `<map>` `<object>` `<q>` `<samp>` `<script>` `<select>` `<small>` `<span>` `<strong>` `<sub>` `<sup>` `<textarea>` `<time>` `<tt>` `<var>`

---

### `<div>` 元素

`<div>`元素通常作为其他HTML元素的容器, 它没有必须的属性, 但是`style`, `class`和`id`是常见的

---

### `<span>` 元素

`<span>` 元素通常作为某些文本的容器

---

## HTML class类属性

`class` 属性为HTML元素指定一个或多个类名, CSS和JavaScript可以使用类名来为具有指定类名的元素执行某些任务, 在CSS中, 要选择具有特定类的元素, 用 `.` 字符后跟类的名称

```html
<style>
.city {
    background-color: tomato;
    color: white;
    padding: 10px;
} 
</style>

<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>
```

> class属性可用于任何HTML元素
> 类名区分大小写

---

### 多个类

HTML 元素可以有多个类名, 每个类名必须用空格分割

---

## HTML id属性

`id` 属性指定HTML元素唯一的ID

---

## HTML iframe (网页中显示网页)

使用`<iframe>`标记定义 HTML iframe:

```html
<iframe src="URL"></iframe>
```

使用`height`和`width`属性指定iframe的大小, 单位是像素, 也可以是百分比

或者使用CSS来设置iframe的高度和宽度

默认情况下, iframe周围有边框, 使用`style`的CSS`border`属性来删除

### iframe链接的按钮

可以点击链接,然后立即在框架中打开, `target`链接的属性必须引用iframe的`name`属性

```html
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>

<p><a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>
```

---

## HTML JavaScript

JavaScript使HTML页面更具有动态性和交互性

---

## HTML 头

### HTML `<head>` 元素

`<head>` 元素是元数据的容器 (关于数据的数据), 放置在`<html>`标签和`< body>`之间, 通常定义文档标题, 字符集, 样式, 链接, 脚本和其他元信息:

`<title>`, `<style>`, `<meta>`, `<link>`, `<script>`, `<base>`

---

### HTML `<title>` 元素

`<title>`元素定义文档的标题, 且在所有HTML/XHTML文档中都是必须的

- 在浏览器选项卡中定义标题
- 在将页面添加到收藏夹时为页面提供标题
- 在搜索引擎结果中显示该页面的标题

---

### HTML `<style>` 元素

`<style>` 元素用于定义单个HTML页面的样式信息:

---

### HTML `<link>` 元素

`<link>` 元素用于链接到外部样式表

```html
<link rel="stylesheet" href="mystyle.css">
```

---

### HTML `<meta>` 元素

`<meta>` 元素用于指定使用的字符集, 页面描述, 关键字, 作者和其他元数据

```html
<!-- 字符集 -->
<meta charset="UTF-8">

<!-- 网页描述 -->
<meta name="description" content="Free Web tutorials">

<!-- 搜索引擎定义关键字 -->
<meta name="keywords" content="HTML, CSS, XML, JavaScript">

<!-- 页面作者 -->
<meta name="author" content="John Doe">

<!-- 每30秒刷新一次文档 -->
<meta http-equiv="refresh" content="30">
```

---

### 设置视口

HTML5 引入了一种方法, 让Web设计人员通过`<meta>`标记控制视口.

视口是用户在网页上的可见区域, 它随设备而变化, 在手机上比在电脑屏幕上小

`<meta>`在所有网页中包含以下视口元素

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

一个`<meta>`视口元素对如何控制网页的尺寸和缩放浏览器的说明.

width = device-width 将页面宽度设置为遵循设备的屏幕宽度 (具体取决于设备)

initial-scale = 1.0 设置浏览器首次加载页面时的初始缩放级别

---

### HTML `<script>` 元素

`<script>` 元素用于定义客户端JavaScript

---

### HTML `<base>` 元素

`<base>` 元素指定页面中所有相对URL的基本打开方法

```html
<base href="https://www.w3schools.com/images/" target="_blank">
```

### 省略`<html>` `<head>` `<body>`

HTML5标准可以省略这三个标签, 但是不建议这么做, 虽然现在有很多人省略`<head>`

---

## HTML 布局

### 布局元素

网站通常以多列(如杂志或报纸)显示内容, HTML5提供了定义网页不同部分的新语义元素

- `<header>` - 定义文档标题 
- `<nav>` - 定义导航链接的容器
- `<section>` - 定义文档中的部分
- `<article>` - 定义一个独立的文章
- `<aside>` - 定义除内容之外的内容(如侧边栏)
- `<footer>` - 为文档或部分定义页脚
- `<details>` - 定义其他详细信息
- `<summary>` - 定义`<details>`元素的标题

---

### HTML 布局技术

创建多列布局有四种不同的方法, 每种方法都有其优点和缺点

- HTML表格(不推荐)
- CSS浮动属性
- CSS flexbox
- CSS框架

---

#### HTML表格

`<table>`元素不是设计为布局工具! `<table>` 元素的目的是显示表格数据, 所以不要使用表格进行页面布局! 它们会给你的代码带来麻烦.

#### CSS框架

使用W3.CSS 或者 Bootstrap等框架

#### CSS浮动

使用CSS浮动属性执行整个Web布局是很常见的, Float易于学习 - 你只需要记住浮动和清楚属性的工作原理. **缺点:** 浮动元素与文档流相关联, 这可能会损害灵活性

#### CSS Flexbox

Flexbox是CSS3中的一种新布局模式

当页面布局必须适应不同的屏幕尺寸和不同的显示设备时, 试用flexbox可确保元素的行为可预测. **缺点:** 在IE10及更早版本中不起作用

---

## HTML响应式网页设计

响应式Web设计是关于使用HTML和CSS自动调整大小, 隐藏, 缩放, 使其在所有设备(台式机, 平板电脑和手机)上看起来都很好

> 任何设备都应该看起来不错!

### 设置视口

制作响应式网页时, 请`<meta>`在所有网页添加以下元素:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

这将设置页面的视口, 这将为浏览器提供有关如何控制页面尺寸和缩放的说明

---

### 响应式图像

响应式图像是可以很好地缩放以适合浏览器大小的图像

#### 使用width属性

如果CSS `width`属性设置为100%, 则图像将响应并向上和向下扩展

```html
<img src="img_girl.jpg" style="width:100%;">
```

在上面的设置中, 图像可以放大到大于其原始大小, 在许多情况下, 更好的解决方案是使用`max-width`属性, 如果`max-width`属性设置为100%, 则图像将缩小(如果必须), 但从不缩放到大于其原始大小

```html
<img src="img_girl.jpg" style="max-width:100%;height:auto;">
```

---

### 根据浏览器宽度显示不同的图像

HTML `<picture>`元素允许你为不同的浏览器窗口大小定义不同的图像

```html
<picture>
  <source srcset="img_smallflower.jpg" media="(max-width: 600px)">
  <source srcset="img_flowers.jpg" media="(max-width: 1500px)">
  <source srcset="flowers.jpg">
  <img src="img_smallflower.jpg" alt="Flowers">
</picture>
```

---

### 响应文本

可以使用"vm"单位设置文本大小, 这意味着"视口宽度"

这样文本大小将遵循浏览器窗口的大小

```html
<h1 style="font-size:10vw">Hello World</h1>
```

调整浏览器窗口的大小以查看文本大小的缩放方式。

在调整文本大小时使用“vw”单位。10vw将大小设置为视口宽度的10％。

> Viewport是浏览器窗口大小, 1vm = 视口宽度的1%, 如果视口宽50厘米, 则1vm为0.5厘米

---

### 媒体查询

除了调整文本和图像的大小之外, 在响应式网页中使用媒体查询也很常见

使用媒体查询, 你可以为不同的浏览器大小定义完全不同的样式

```html
<style>
.left, .right {
  float: left;
  width: 20%; /* The width is 20%, by default */
}

.main {
  float: left;
  width: 60%; /* The width is 60%, by default */
}

/* Use a media query to add a breakpoint at 800px: */
@media screen and (max-width: 800px) {
  .left, .main, .right {
    width: 100%; /* The width is 100%, when the viewport is 800px or smaller */
  }
}
</style>
```

### 使用W3.CSS 或者 bootstrap框架

---

## HTML 代码元素

- `<code>` 元素定义了计算机代码片段, 因为无法有额外空行和空格, 外面可以包`<pre>`
- `<kbd>` 一般用于键盘输入的内容
- `<samp>` 元素表示来自程序或计算系统的输出
- `<var>` 元素定义一个变量

---

## HTML 实体字符

HTML有的保留字符必须替换为字符实体,否则无法正常显示, 因为与标记混合

| Result | Description | Entity Name | Entity Number |
|--- | --- | --- | --- | 
| ` ` | `non-breaking space` | `&nbsp;` | `&#160;` |
| `<` | `less than` | `&lt;` | `&#60;` |
| `>` | `greater than` | `&gt;` | `&#62;` |

> 实体名称区分大小写

---

## HTML 字符集

HTML4

```html
<meta http-equiv="Content-Type" content="text/html;charset=ISO-8859-1">
```

HTML5

```html
<meta charset="UTF-8">
```

CSS样式表的字符集

```css
@charset "UTF-8";
```

---

### HTML 统一资源定位符

---

URL是网址的另一个词, URL可以由单词(w3schools.com) 或Internet协议(IP)地址(192.68.20.50)组成

大多数人在冲浪时输入名称, 因为名字比数字更容易记住

```
scheme://prefix.domain:port/path/filename
```

- scheme - 定义internet服务的类型 (最常见的是http或https)
- prefix - 定义域前缀 (www)
- port - 定义主机上的端口号 (默认80 可省略)
- path - 在服务器上定义路径(如果省略, 就是站点的根目录)
- filename - 定义文档或资源的名称

---

### 常见的URL方案


