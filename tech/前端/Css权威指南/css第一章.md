### Media Descriptors

```css
@import url(print-color.css) print and (color);
```

```html
<link
  href="print-color.css"
  type="text/css"
  media="print and (color), screen and (color-depth: 8)"
  rel="stylesheet"
/>
```

 每个媒体特性描述符括在括号中。如果没有提供媒体类型，则假设为 all， 

 and 

 将两个或多个媒体特性链接在一起，使所有特性都为真，查询才为真 

 not 

 否定整个查询，如果所有条件都为真，则不应用样式表。  not 关键字只能在媒体查询的开头使用。 

   没有用于媒体查询的 OR 关键字。 。相反，分隔查询列表的逗号具有 or - screen 的功能， 

 only，它被设计成故意向后 不兼容  只能用于开头，能理解这些媒体，就执行，不能理解就不执行

### 特征查询  

查询看支不支持，

```css
@supports (color: black) {
  body {
    color: black;
  }
  h1 {
    color: purple;
  }
  h2 {
    color: navy;
  }
}
```

响应式布局

```css
@media screen and (max-width: 30em) {
  @supports (display: flex) {
    /* small-screen flexbox styles go here */
  }
}
@media screen and (min-width: 30em) {
  @supports (display: flex) {
    /* large-screen flexbox styles go here */
  }
}
```

and

```css
@supports (display: grid) and (shape-outside: circle()) {
  /* grid-and-shape styles go here */
}
```

```css
@supports (display: grid) {
  @supports (shape-outside: circle()) {
    /* grid-and-shape styles go here */
  }
}
```

or

```css
@supports (shape-outside: circle()) or (-webkit-shape-outside: circle()) {
  /* shape styles go here */
}
```

not 

```css
@supports not (display: grid) {
  /* grid-not-supported styles go here */
}
```

  括号来保持逻辑的正确性, 需要那些额外的括号。没有它们，整个表达式将失败，块内的样式将被跳过。  :支持颜色时应用一组样式，在支持网格或灵活的框布局时应用一组样式 

```css
@supports (color: black) and ((display: flex) or (display: grid)) {
  /* styles go here */
}
```

 特性查询测试需要属性和值 