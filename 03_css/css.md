# CSS 

> CSS 是一种描述HTML文档样式的语言
> CSS 描述了如何显示HTML元素

## CSS 简介

---

### 什么是CSS?

- CSS就是层叠样式表
- 描述了如何在屏幕, 纸张或者其他媒体上显示HTML元素
- 节省了大量的工作, 可以同时控制多个网页的布局
- 外部样式表村粗在CSS文件中

---

## CSS语法和选择器

### CSS语法

CSS由选择器和生命快组成

选择器指向要设置样式的HTML元素

声明块包含一个或多个以分号分割的声明, 每个声明都包含一个CSS属性名称和一个以冒号分割的值, 以分号结尾, 声明块用花括号括起来.

---

## CSS工作方式

- 外链式
- 内链式
- 行内式

---

## CSS颜色

目前采用RGB十六进制方式

---

## CSS背景

`background-color`属性指定元素的背景颜色。

```css
body {
    background-color: lightblue;
}
```

`background-image`属性指定要用作元素背景的图像。

默认情况下，图像会重复，因此它会覆盖整个元素。

`background-repeat: repeat-x;`水平重复

`background-repeat: repeat-y;` 垂直重复

图像的位置由`background-position`属性指定：

```css
body {
    background-image: url("img_tree.png");
    background-repeat: no-repeat;
    background-position: right top;
}
```

背景图片 - 固定位置请使用以下`background-attachment`属性：

```css
body {
    background-image: url("img_tree.png");
    background-repeat: no-repeat;
    background-position: right top;
    background-attachment: fixed;
}
```

使用速记属性时`background`，属性值的顺序为：

- `background-color`
- `background-image`
- `background-repeat`
- `background-attachment`
- `background-position`

---

## CSS边框

CSS `border`属性允许您指定元素边框的样式，宽度和颜色。