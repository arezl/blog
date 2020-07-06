

## 基本样式规则

<font color="gray">This is h2 text</font>

### 元素选择器 Element Selectors

### 声明和关键字

 声明中使用了错误的属性或值，整条规则都会被忽略 

```css
p {
  font: medium Helvetica;
}
```

 当然不存在`rainbow`这个属性，它只是被当做例子来进行说明。`rainbow`的值是`red orange yellow green blue indigo violet`，这 7 个关键字放在一起组成了一个唯一的值。我们可以像下面这样重新定义`rainbow`的值 

 如我们所见。CSS 关键字通常使用空白分隔。在 CSS2.1 中有个例外：`font`属性值可以使用正斜杠（`/`）分隔两个特殊的关键字 

 斜线分隔的关键字设置元素的字体大小和行高， 

 多背景图片、过渡和阴影，声明时使用逗号分隔。另外函数参数，如`linear gradiennts`和`transform`等，也使用逗号分隔 



## 组合 Grouping
如果你想让h2元素和段落都显示灰色文本，最简单的方式是使用下面的声明：

h2,
p {
  color: gray;
}
去掉逗号，会使语句变成“后代选择器”
通配符选择器 The universal selector
（*）标注。这个选择器就像一张百搭牌，可以匹配所有元素

### 组合声明 Grouping Declarations

 要注意写组合声明时每条声明后面的分号都至关重要 

就是一个标签下可以设置多条属性

### 旧浏览器中的新元素 New Elements in Old Browsers

```js
document.createElement("main");
```

 下面这行 JavaScript 代码告诉 IE8 `main`元素的存在 

## 2.3 类和 ID 选择器 Class and ID Selectors

 **类选择器**和 **ID 选择器** 

 当只有整个段落是警告时，才设置为粗体 

```css
p.warning {
  font-weight: bold;
}
```

 另一种做法是使用一个通用的类选择器和一个特定元素的类选择器，来让样式更加实用， 

```css
.warning {
  font-style: italic;
}
span.warning {
  font-weight: bold;
}
```

 想选择具有某个类名的所有元素，省略通配选择器不会有任何影响 

###  多个类 Multiple Classes

```html
<p class="urgent warning">
  When handling plutonium, care must be taken to avoid the formation of a
  critical mass.
</p>
```

 （`class`值中）单词的顺序没有影响，写成`warning urgent`会产生完全相同的结果。 

 假如你想让所有`class`值为`warning`的元素加粗，把`class`值为`urgent`的设为斜体，而同时包含两个值的元素设置银色背景，写法是这样： 

```css
.warning {
  font-weight: bold;
}
.urgent {
  font-style: italic;
}
.warning.urgent {
  background: silver;
}
```

 多类选择器里面包含一个无空格分隔的类名，匹配将会失效 

```css
p.warning.help {
  background: red;
}
```

```html
<p class="urgent warning help">Help me!</p>
```

只会匹配如上内容

### ID 选择器 ID Selectors

  这个值会出现在每个文档中的某个随机的元素上，而且在每个文档中仅出现一次 

 类可以分配给任意多的元素，类名`warning`可以分配给一个`p`元素或者一个`span`元素，或者更多其他元素。然而，ID 在一个 HTML 文档中使用且仅使用一次。因此如果有了一个`id`值为`lead-para`的元素，该文档中的其他元素都不能有`lead-para`的`id`值 

 与类选择器不同，ID 选择器不能联合使用，因为 ID 属性不允许使用空白分隔的单词列表。 .

，ID 有更高的权重。 类和 ID 选择器的大小写要和文档中的匹配。

### 2.4.2 基于准确属性值选择

```css
a[href="http://www.css-discuss.org/about.html"]
{
  font-weight: bold;
}
```

[foo~="bar"]	选择所有带有foo属性、且foo属性被空白分隔的单词列表中含有单词bar的元素。
[foo*="bar"]	选择所有带有foo属性、且foo属性值中含有子串bar的元素。
[foo^="bar"]	选择所有带有foo属性、且foo属性值以bar开头的元素。
[foo$="bar"]	选择所有带有foo属性、且foo属性值以bar结束的元素。
[foo&#124;="bar"]	选择所有带有foo属性、且foo属性值以bar开头后接一个短线（U+002D）或者属性值是bar的元素。
#2.4.4 A Particular Attribute Selection Type 特定的属

```css
*[lang|="en"] {
  color: white;
}
```

 任何`lang`属性等于`en`或者以`en-`开头的元素。 

```css
*[class|="btn"] {
  border-radius: 5px;
}
```

 注意选择器中的波浪线（~），这是基于属性值中分离单词进行选择的关键字。如果忽略了波浪线，选择器就变成了前面讨论过的精确值匹配的属性选择器。 

 `p.warning`和`p[class~="warning"]`是相等同的 

 你可以使用匹配部分属性值的选择器选择`title`属性的文字，来选中那些是图表的图片 、

```css
img[title~="Figure"] {
  border: 1px solid gray;
}
```

```css
span[class*="cloud"] {
  font-style: italic;
}
```

 为所有到 O'Reilly Media 网页的链接添加特殊样式 

```css
a[href*="oreilly.com"] {
  font-weight: bold;
}
```

```css
a[href^="https:"] {
  font-weight: bold;
}
a[href^="mailto:"] {
  font-style: italic;
}
```

 [title^="Monday"] 



 最常见的使用场景是基于链接的资源类型添加样式，例如图 2-14 所示，为指向 PDF 文档的链接添加特定样式。 

```css
a[href$=".pdf"] {
  font-weight: bold;
}
```

 上一节中日程的例子，可以基于给定的年份选择所有对象，使用一个类似这样的选择器`[title$="2015"]`。 

 ***了安全，建议在任何情况下都为属性选择器中的属性值添加引号，尽管只有非法标识符导致它需要被标记成字符串的时候引号才是必需的。*** 

```css
a[href$='.PDF' i]忽略大小写选项 它只用于属性选择器的值，而不能用于属性名本身
```

### 后代选择器



```css
h1 em {
  color: gray;
}
```

 在……中”、“是……的一部分”或“是……的后代”，前提是选择器从右向左读。 

 ***`:link`选择那些尚未被访问过的资源链接*** 

 后代选择器的一个容易被忽略的地方是，元素和后代元素之间可以间隔无限代其他元素。 

 例如选择一个是`h1`元素的子元素（而不是任意后代元素）的`strong`元素，这种情况下，可以使用子元素组合器，它是一个大于号（`>`）: 

```css
h1 > strong {
  color: red;
}
```

 一个紧跟着标题的段落设置样式，或者给一个紧跟着段落的列表添加一个边距，可以使用**相邻兄弟组合器**来选择在同一个父级元素下紧跟着另一个元素的元素，组合器使用加号（`+`）。就像子元素选择器一样，这个符号也可以在两边添加或省略空格。 



```css
h1 + p {
  margin-top: 0;
}
```

 选择器读作：“选择任何紧跟在`h1`元素后面的`p`元素” 

 如果写作`li + li {font-weight: bold;}`,只有每个列表中的第二项和第三项会被设置为粗体，样式不会对第一项生效 

 了一个新的兄弟组合器叫做**一般兄弟选择器**。这个组合器允许选择同一个父元素下，跟随（不一定是紧跟随）在某个元素后面的所有元素，使用波浪线符号（`~`） 

 为同一个父元素下跟随在一个`h2`元素后面的任何`ol`元素设置斜体，可以写作`h2 ~ ol {font-style: italic;}`。两个`ol`元素不必都是紧邻兄弟，尽管紧邻兄弟也会被这条规则匹配。效果见图 2-22. 

 在开始之前，先提一下“链式”。CSS 允许（链式）组合伪类选择器，例如，当鼠标停留在（`hover`）一个未访问过的链接（``）上时，将其设置为红色，当鼠标停留在已经访问过的链接上时,将其设置为栗色： 

```css
a:link:hover {
  color: red;
}
a:visited:hover {
  color: maroon;
}
```

 `#ericmeyer:first-child.`。问题是这个选择器选择的是我，而且只有当我是我父母的第一个孩子的时候才会选择我（巧了，我还真是）。如果要选择我的第一个孩子，选择器应该是`#ericmeyer > :first-child` 

> 伪类的作用是给它们绑定的元素添加一些“影子类”，就不容易犯（前面的）错误了。

#### [#](http://gdut_yy.gitee.io/doc-csstdg4/ch2.html#选中根元素-selecting-the-root-element)选中根元素 Selecting the root element

 这是结构简单性的精髓：伪类选择器`:root`选择文档的根元素 

 使用伪类`:empty`，可以选择任何没有子节点的元素——没有任何类型的子元素：**包含**文本节点，包括文字和空白。这有助于筛除 CMS 生成的没有填进任何实际内容的元素。因此，`p:empty {display: none;}`将会让所有空的段落不再显示。 

 你可能会试着为所有空元素设置样式，像这样：`*:empty {display: none;}`，但是这里有个潜在的陷阱：`:empty`会匹配 HTML 的空元素，如`img`和`input`，甚至会匹配`textarea`，除非你为`textarea`元素插入了一些默认文本。因此，从匹配元素的角度来说，`img`和`img:empty`是一样的（它们在特度上有区别，我们将在下一章讨论 

> 如果您想选中所有由超链接元素包装的图像，:only-child 伪类适合您。 当它们是父元素中的唯一元素时，它将会被选中。 所以如果你想给父元素中唯一图像元素增加外框。 您可以这样写：

 如果您的段落包含一个图像而没有其他子元素，无论周围的所有文本如何，都将选中该图像。 

```css
img:only-child {
  border: 1px solid black;
}
```



```css
a[href] img:only-child {
  border: 2px solid black;
}
```

```html
<a href="http://w3.org/"><img src="w3.png" alt="W3C" /></a>
<a href="http://w3.org/"><img src="w3.png" alt="" /> The W3C</a>
<a href="http://w3.org/"><img src="w3.png" alt="" /> <em>The W3C</em></a>
```

 only-child，有两件事要记住。 首先唯一子元素伪类总是应用于子元素，而不应用于父元素，这在前面已经解释过了。 相对应要记住的第二件事，就是当您在后代选择器中使用:only-child 时，不用严格列出元素之间的父子关系 

 这一个元素具有两个子元素：b 和 img。 该图像不再是其父级（超链接）的唯一子级，因此无法使用:only-child 进行匹配。 但是，可以使用:only-of-type 进行匹配。 如图 2-26 所示 

```css
a[href] img:only-of-type {
  border: 5px solid black;
}
```

 两者的不同在于，:only-of-type 将会在所有同级元素中匹配指定类型的元素，而:only-child 只匹配没有其它同级元素的元素 

> 这在某些情况下非常有用，例如在段落中选中图像，用这种做法不必担心超链接或其他内联元素的影响。

```css
p > img:only-of-type {
  float: right;
  margin: 20px;
}
```

only 只表示标签元素

```css
p:first-child {
  font-weight: bold;
}
li:first-child {
  text-transform: uppercase;
}
```

 :first-child 相对应的是:last-child。 如果我们采用前面的示例 

```css
table:first-of-type {
  border-top: 2px solid gray;
}
```

type 最后一个，不一定最后一个就是 table都可以。

```css
<tr>
  <th scope="row">Count</th><td>7</td><td>6</td><td>11</td>
</tr>
<tr>
  <td>Q</td><td>X</td><td>-</td>
</tr>
```

```css
td:first-of-type {
  border-left: 1px solid red;
}
```

```css
table:only-of-type {
  color: red;
}
table:first-of-type:last-of-type {
  background: red;
}
```

 让我们从与:first-child 等效的:nth-child（1）入手讲述:nth-child（）。 在以下示例中，所选元素将是第一段和第一列表项。 

```css
p:nth-child(1) {font-weight: bold;}
li:nth-child(1) {text-transform: uppercase;}
<div>
  <p>These are the necessary steps:</p>
  <ul>
    <li>Insert key</li>
    <li>Turn key <strong>clockwise</strong></li>
    <li>Push accelerator</li>
  </ul>
  <p>
    Do <em>not</em> push the brake at the same time as the accelerator.
  </p>
</div>
```

 更强大的是，您可以使用 n + b 或 n - b 形式的简单代数表达式来定义重复出现的实例，其中 a 和 b 是整数，n 用于倍数。 此外，+ b 或-b 是可选的，因此在不需要时可以将其删除。  

可以选择第一和第四项： 

```css
ul > li:nth-child(3n + 1) {
  text-transform: uppercase;
}
```

 ![img](http://gdut_yy.gitee.io/doc-csstdg4/figures/ch2/fg2-32.png) 

  n 代表级数 0、1、2、3、4，然后无限大。 然后，浏览器求解 3n +1，得出 1、4、7、10、13，依此类推。 如果我们放弃+1，因此只剩下 3n，结果将是 0、3、6、9、12，依此类推 

 定元素计数以 1 开始，得出：nth-child（2n）将选择偶数个孩子，而：nth-child（2n 1）或：nth-child（2n-1）是选择奇数的一个小技巧。您可以将它记着，或者使用 nth-child（）接受的两个特殊关键字：偶数和奇数。 如果想要突出表中的奇数行（从第一行开始）？ 方法如下，结果如图 2-33 所示：

 第九个开始的所有行， 

```css
tr:nth-child(n + 9) {
  background: silver;
}
tr:nth-child(8) ~ tr {
  background: silver;
}
```

```css
tr:nth-last-child(odd) {
  background: silver;
}
tr:nth-last-child(2n + 1) {
  background: silver;
} /
```

```css
li:nth-child(3n + 3) {
  border-left: 5px solid black;
}
li:nth-last-child(4n - 1) {
  border-right: 5px solid black;
  background: silver;
}
```

 ![img](http://gdut_yy.gitee.io/doc-csstdg4/figures/ch2/fg2-34.png)  

```css
li:only-child {
  width: 100%;
}
li:nth-child(1):nth-last-child(2),
li:nth-child(2):nth-last-child(1) {
  width: 50%;
}
li:nth-child(1):nth-last-child(3),
li:nth-child(1):nth-last-child(3) ~ li {
  width: 33.33%;
}
li:nth-child(1):nth-last-child(4),
li:nth-child(1):nth-last-child(4) ~ li {
  width: 25%;
}
```

 在这些示例中，如果列表项是唯一的列表项，则宽度为 100％。 如果列表项是第一项，也是从倒数第二项，则意味着有两个项，并且宽度为 50％。 如果一个项目是第一个项目，也是最后一个项目的第三个项目，则我们将其制成，其后的两个同级列表项目的宽度为 33％。 类似地，如果列表项是第一项，也是最后一项的第四项，则意味着恰好有四个项目，因此我们将其及其三个同级产品制成 25％宽度。 

```css
p > a:nth-of-type(even) {
  background: blue;
  color: white;
}
```

 :nth-of-type(1) :nth-last-of-type(1)，以更高的特异性重新声明：only-of-type。 

 required 与任何必填的表单控件匹配。 :optional 伪类与没有必需属性或者其必需属性的值为 false 的表单控件匹配 

input[required] {
  border: 1px solid #f00;
}
input:not([required]) {
  border: 1px solid #ccc;
}

 其中将一个图像放置到所有具有焦点的电子邮件 input 的背景中，其中一个图像在输入无效时使用，另一幅在输入有效时使用 

```css
input[type="email"]:focus {
background-position: 100% 50%;
background-repeat: no-repeat;
}
input[type="email"]:focus:invalid {
background-image: url(warning.jpg);
}
input[type="email"]:focus:valid {
background-image: url(checkmark.jpg);
}
<input type="email">
```

```
input[type="number"]:focus {
background-position: 100% 50%;
background-repeat: no-repeat;
}
input[type="number"]:focus:out-of-range {
background-image: url(warning.jpg);
}
input[type="number"]:focus:in-range {
background-image: url(checkmark.jpg);
}
<input id="nickels" type="number" min="0" max="1000" />
```

可变伪类包括：:read-write，它是指用户可编辑的用户输入；和:read-only，与不可编辑的用户输入匹配。只有能够通过用户输入更改的元素才能被:read-write 匹配

非禁用的非只读 input 元素是:read-write，任何具有 contenteditable 属性的元素也是如此。 其他所有元素都被:read-only 匹配	

给定的选择器中仅允许使用一个伪元素

```css
p:first-of-type::first-letter {
  font-size: 200%;
}
```

### 在元素前后添加内容 Styling (or Creating) Content Before and After Elements

 CSS 允许您插入生成的内容，然后直接使用伪元素:: before 和:: after 设置样式。 图 2-47 给出了一个示例。 

