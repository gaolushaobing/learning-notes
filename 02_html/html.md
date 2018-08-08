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