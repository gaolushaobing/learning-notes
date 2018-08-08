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

`alt`

