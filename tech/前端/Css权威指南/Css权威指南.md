> 层叠样式表(Cascading Style Sheets, CSS)是一种强大的工具，它可以转换文档或文档集合的格式，而且它已经扩展到 web 的几乎每个角落，并进入许多表面上没有 web 的环境。例如，基于 gecko 的浏览器使用 CSS 来影响浏览器 chrome 本身的表现，许多 RSS 客户端允许您将 CSS 应用于提要和提要条目，一些即时消息客户端使用 CSS 来格式化聊天窗口。CSS 的各个方面可以在 JavaScript 框架使用的语法中找到，甚至在 JavaScript 本身中也可以找到。到处都是!
> CSS 最初是在 1994 年提出的，当时 web 刚刚开始流行。当时，浏览器为用户提供了各种样式设置功能——例如，Mosaic 中的表示首选项允许用户在每个元素的基础上定义各种字体、大小和颜色。这些对文档作者都是不可用的;他们所能做的就是将一段内容标记为段落、某个级别的标题、预先格式化的文本或少数其他元素类型之一。如果一个用户配置他的浏览器使所有一级的标题都是小的和粉红色的，而所有六级的标题都是大的和红色的，那么，这就是他的问题了。
> CSS 就是在这种环境中引入的。它的目标是提供一种简单的、声明式的样式语言，这种语言对作者来说是灵活的，最重要的是，它为作者和用户都提供了样式功能。通过“级联”的方式，这些风格可以被组合在一起并按优先级排列，这样作者和读者都有发言权——尽管读者总是拥有最后的发言权。
> 工作进展迅速，到 1996 年年底，CSS1 已经完成。当新成立的 CSS 工作组推进 CSS2 时，浏览器却难以以互操作的方式实现 CSS1。尽管每个 CSS 片段本身相当简单，但是这些片段的组合创建了一些令人惊讶的复杂行为。在早期的实现中也有一些不幸的失误，比如 box 模型实现中臭名昭著的差异。这些问题威胁着 CSS 的发展，但幸运的是，一些聪明的建议得以实施，浏览器开始协调起来。在几年之内，由于增强的互操作性和引人注目的发展，例如基于 CSS 的 Wired 杂志的重新设计和 CSS Zen Garden, CSS 开始流行起来。
> 然而，在这一切发生之前，CSS 工作组已经在 1998 年初确定了 CSS2 规范。CSS2 完成后，立即开始 CSS3 的工作，并将 CSS2 的一个明确版本称为 CSS2.1。为了顺应时代精神，CSS3 被构建为一系列(理论上)独立的模块，而不是单一的单一规范。这种方法反映了当时处于活动状态的 XHTML 规范，出于类似的原因，该规范被划分为多个模块。
> 模块化 CSS3 的基本原理是，每个模块都可以按照自己的速度工作，而且特别重要的(或流行的)模块可以按照 W3C 的进度前进，而不会受到其他模块的阻碍。事实上，事实就是如此。到 2012 年初，三个 CSS3 模块(以及 CSS1 和 CSS 2.1)已经达到了完全推荐状态——CSS 颜色级别 3、CSS 名称空间和选择器级别 3。与此同时，有 7 个模块处于候选推荐状态，其他几十个模块处于不同的工作草拟阶段。在旧的方法下，颜色、选择器和名称空间必须等到规范的其他部分完成或删除之后才能成为完整规范的一部分。由于模块化，他们不必等待。
> 这种优势的另一面是，很难谈论一个“CSS3 规范”。“没有这种东西，也不可能有。即使其他所有的 CSS 模块在 2016 年末达到了第 3 级(他们没有)，已经有了第 4 级的选择器。我们会把它称为 CSS4 吗?还有哪些“CSS3”特性仍在发挥作用?或者网格布局，甚至还没有达到一级?
> 因此，虽然我们不能指着一本大部头说“有 CSS3”，但我们可以通过介绍这些功能的模块名称来谈论它们。这些灵活性模块不仅弥补了它们有时造成的语义上的尴尬。(如果你想要一个近似于单一规范的东西，CSS 工作组每年都会发布“快照”文档。)
> 有了这些，我们就可以开始理解 CSS 了。不过，我们必须先检查一下标记。
> 元素是文档结构的基础。在 HTML 中，最常见的元素很容易识别，如 `p`, `table`, `span`, `a`, 和 `div`。文档中的每个元素都在其表示中起作用。
> 虽然 CSS 依赖于元素，但并不是所有的元素都是平等创建的。例如，图像和段落不是同一类型的元素，`span` and `div` 也不是。在 CSS 中，元素通常有两种形式:替换和非替换。
> 被替换的元素是那些元素的内容被文档内容没有直接表示的内容所替换的元素。最熟悉的 HTML 示例可能是 img 元素，它被文档本身外部的图像文件所取代。事实上，img 并没有实际的内容，你可以在这个简单的例子中看到:
>
> 这个标记片段只包含一个元素名和一个属性。元素不会显示任何内容，除非您将其指向某些外部内容(在本例中，是由 src 属性指定的图像)。如果您指向一个有效的图像文件，则图像将被放置在文档中。如果没有，它将不显示任何内容，或者浏览器将显示一个“损坏的图像”占位符。
> 类似地，input 元素也可以替换为单选按钮、复选框或文本输入框，这取决于它的类型。
>hi there</span>` is a nonreplaced element, and the text “hi there” will be displayed by the user agent. This is true of paragraphs, headings, table cells, lists, and almost everything else in HTML.
> 大多数 HTML 元素是不可替换的元素。这意味着它们的内容由用户代理(通常是浏览器)在元素本身生成的框中显示。例如，`<span>hi there</span>` 是一个不可替换的元素，文本“hi there”将由用户代理显示。这适用于 HTML 中的段落、标题、表格单元格、列表和几乎所有其他内容。
> 除了替换和非替换元素外，CSS 还使用了其他两种基本类型的元素:块级和行内级。还有更多的显示类型，但这些是最基本的，也是大多数(如果不是所有)其他显示类型所引用的类型。对于那些花时间研究 HTML 标记及其在 web 浏览器中的显示的作者来说，块类型和内联类型是很熟悉的。这些元素如图 1-1 所示。
>Block- and inline-level elements in an HTML document</Figures>
> 块级元素生成一个元素框，该元素框(默认情况下)填充其父元素的内容区域，并且不能在其两侧有其他元素。换句话说，它在元素框之前和之后生成“break”。HTML 中最常见的块元素是 p 和 div。被替换的元素可以是块级别的元素，但通常不是。
> 列表项是块级元素的特殊情况。除了以与其他块元素一致的方式工作外，它们还生成一个标记(通常是无序列表的项目符号和有序列表的数字)，该标记被“附加”到元素框中。除了此标记之外，列表项在其他所有方面都与其他块元素相同。
> 内联级元素在一行文本中生成一个元素框，并且不会破坏该行的流。最好的内联元素示例是 HTML 中的 a 元素。这些元素不会在它们自己之前或之后生成“break”，因此它们可以出现在另一个元素的内容中，而不会中断它的显示。
> 请注意，虽然“块”和“内联”的名称与 HTML 中的块级和内联级元素有很多相同之处，但它们之间有一个重要的区别。在 HTML 中，块级元素不能从内联级元素派生。在 CSS 中，对于显示角色之间如何嵌套没有限制。为了了解它是如何工作的，让我们考虑一个 CSS 属性 display。
> 为了了解它是如何工作的，让我们考虑一个 CSS 属性 display。
> 你可能已经注意到了这里有许多取值，只有其中三个是我提到过的：`block`、`inline`和`list-item`。这些取值的大部分会在本书其他部分介绍；例如`grid`和`inline-grid`涵盖在介绍栅格布局的独立的一章，跟表格相关的值都包含在介绍 CSS 表格布局的章节中。
> 现在我们把注意力放在`block`和`inline`上，看下面的代码：
>
>This is a paragraph with <em>an inline element</em> within it.</p>
>
> 这里有两个块级元素（`body`和`p`）和一个行内元素（`em`）。根据 HTML 规范，`em`可以作为`p`的后代，但反过来则不行。通常 HTML 的层级结构允许行内元素作为块级元素的后代，而不是相反。
> CSS 则没有这样的限制，你可以保持现有的标签结构，然后修改这两个元素的显示角色：
> 这使得元素在一个行内框里面生成了一个块级框，这在 CSS 中是完全合法的，不会破坏任何规范。但是，如果你想在 HTML 中使用相反的嵌套结构，那就有会问题了，像这样：
><p>This is a paragraph improperly enclosed by an inline element.</p></em>
> 不管你如何使用 CSS 来修改它们的显示角色，这在 HTML 中都是不合法的。
> 修改元素的显示角色在 HTML 文档中很有用，它对 XML 文档也至关重要。XML 文档一般没有默认的显示角色，而完全依赖文档开发者去定义它们。例如，如果你想要展示下面的 XML 片段：
>
>Cascading Style Sheets: The Definitive Guide</maintitle>
>Third Edition</subtitle>
>Eric A. Meyer</author>
>O'Reilly and Associates</publisher>
>November 2006</pubdate>
>978-0-596-52733-4</isbn>
>
>
>CSS Pocket Reference</maintitle>
>Third Edition</subtitle>
>Eric A. Meyer</author>
>O'Reilly and Associates</publisher>
>October 2007</pubdate>
>978-0-596-51505-8</isbn>
>
> 因为`display`属性的默认值是`inline`，所以这块内容会默认被显示为行内文本，就像图 2 所示的那样。这样的排版不太有用。
>Default display of an XML document</Figures>
> 你可以用`display`来定义文档的基本板式：
> 这样把 7 种元素中的 5 个设置成块级元素，2 个设置成行内元素。块级元素会被像 HTML 中的`div`那样处理，两个行内元素会被类似`span`那样处理。
> 因为这种设置显示角色的基本能力，CSS 在各种场景下都非常有用。你可以从上面的规则开始，添加一些更具视觉效果的样式，然后得到像图 3 这样的显示效果。
>Styled display of an XML document</Figures>
> 在详细学习如何编写 CSS 之前，我们先要看一下如何关联 CSS 和文档，毕竟，如果不把它们结合在一起，CSS 是无法对文档起作用的。我们从最熟悉的 HTML 设置开始。
> 我提到过 HTML 文档存在一个固有结构，这一点值得重复一下。实际上有个旧网页开发遗留的问题：我们太多人忘记了文档是应该有一个内在结构的，这与视觉上的结构是完全不同的。我们急于在 Web 上创建看起来最酷的网页，我们改造转换、修饰装点，全然忽视了页面应该包含具有一些结构意义的信息。
> 这种结构是 HTML 和 CSS 之间关系所固有的组成部分，没有它，关系就不会存在。为了更好地理解这种结构，我们把下面这个示例的 HTML 文档拆解来看：
>
>
>Eric's World of Waffles</title>
>
>
>
>
>
>
>Waffles!</h1>
>
>
>
>
> 代码的处理结果及应用的样式的如图 4 所示。
>A simple document</Figures>
> 现在我们来看文档关联 CSS 的几种方式。
>
> `link`标签是一个有些被忽视的标签，但它是在 HTML 规范中存在了许多年的合法标签，一直在等着被善加利用。它最初的目的是允许 HTML 开发者把包含链接标签的文档与其他文档关联起来。CSS 使用`Link`标签把样式表链接到文档中，如图 5，一个名为`sheet1.css`的样式表被连接到文档。
> 这些样式表不是 HTML 文档的一部分但仍被应用于文档中，它们被称为**外部样式表**，因为它们存在于 HTML 文档的外部（看图）。
> 要成功加载外部样式表，`link` 必须放在 `head` 元素中，但不能放在任何其他元素中。这将导致 web 浏览器定位和加载样式表，并使用它包含的任何样式以图 1-5 所示的方式呈现 HTML 文档。图 1-5 还显示了外部`sheet2.css`的加载情况。通过@import 声明。导入必须放在包含它们的样式表的开头，但在其他方面不受约束。
>A representation of how external stylesheets are applied to documents</Figures>
> 那么外部样式表是什么样的格式呢？和我们在前面章节中和在示例 HTML 文档中看到的那些样式一样，外部样式也是简单的规则列表，但是这些规则存储在自己的文件里面。要记住，HTML 和其它任何标记语言都不能放进样式表中——它只能包含样式规则。一个外部样式表的内容是这样的：
> 这就是它的全部内容——没有 HTML 标记或者注释，只有干净简单的样式声明。它们被存储在纯文本文件中，通常用`.css`作为后缀，例如`sheet1.css`。
>An external stylesheet cannot contain any document markup at all, only CSS rules and CSS comments, both of which are explained later in the chapter. The presence of markup in an external stylesheet can cause some or all of it to be ignored.</Tips>
> 对于 link 标记的其余部分，属性和值非常简单。rel 代表“关系”，在本例中，关系是样式表。属性类型总是设置为 text/css。此值描述将使用链接标记加载的数据类型。这样，web 浏览器就知道样式表是一个 CSS 样式表，这将决定浏览器如何处理它导入的数据。毕竟，将来可能还会使用其他样式语言，所以声明您正在使用的 hich 语言是很重要的。
> 接下来，我们找到 href 属性。这个属性的值是你的样式表的 URL。这个 URL 可以是绝对的，也可以是相对的，这取决于什么适合您。在我们的示例中，URL 是相对的。它也可以是类似于http://meyerweb.com/sheet1.css这样的东西。
> 最后，我们有一个媒体属性。此属性的值是一个或多个媒体描述符，它们是关于媒体类型和这些媒体特性的规则，每个规则由逗号分隔。因此，例如，你可以在屏幕和投影媒体中使用链接样式表:
>
>
>
>
>
>
>
>
>
> The one attribute that is not in this example markup, but could be, is the title attribute. This attribute is not often used, but it could become important in the future and, if used improperly, can have unexpected effects. Why? We will explore that in the next section.
> 还可以定义其他样式表。通过使 rel 属性的值成为备选样式表来定义它们，并且只有在用户选择时才在文档表示中使用它们。
> 如果浏览器能够使用替代样式表，它将使用 link 元素的 title 属性的值来生成样式替代列表。你可以这样写:
>
>
>
>A browser offering alternate stylesheet selection</Figures>
>As of late 2016, alternate stylesheets were supported in most Gecko-based browsers like Firefox, and in Opera. They could be supported in the Internet Explorer family through the use of JavaScript but are not natively supported by those browsers. The WebKit family did not support selecting alternate stylesheets. Compare this to the age of the browser shown in Figure 1-6--it’s almost shocking.</Tips>
>
>
>
>
>
>
>
>
>
>`, as shown in the preceding example. This is followed by one or more styles and is finished with a closing `</style>` tag. It is also possible to give the style element a media attribute, which functions in the same manner as previously discussed for linked stylesheets. The styles between the opening and closing style tags are referred to as the document stylesheet or the embedded stylesheet (because this kind of stylesheet is embedded within the document). It will contain many of the styles that will apply to the document, but it can also contain multiple links to external stylesheets using the @import directive.
>
>
>Older versions of Internet Explorer for Windows do not ignore any @import directive, even those that come after other rules. Since other browsers do ignore improperly placed @import directives, it is easy to mistakenly place the @import directive incorrectly and thus alter the display in other browsers.</Tips>
>;rel=stylesheet;type=text/css"
>
>;rel=stylesheet;type=text/css"
>
>There are equivalents to this technique in common scripting languages such as PHP and IIS, both of which allow the author to emit HTTP headers. It’s also possible to use such languages to explicitly write a link element into the document based on the server offering up the document. This is a more robust approach in terms of browser support: every browser supports the link element.</Tips>
>
>
>` will set the text color to be maroon and the background to be yellow for that paragraph only. No other part of the document will be affected by this declaration.
>
>
>
>The structure of a rule</Figures>
>One way to create “nested” comments accidentally is to temporarily comment out a large block of a stylesheet that already contains a comment. Since CSS doesn’t permit nested comments, the “outside” comment will end where the “inside” comment ends.</Tips>
>CSS comments are treated by the CSS parser as if they do not exist at all, and so do not count as whitespace for parsing purposes. This means you can put them into the middle of rules—even right inside declarations!</Tips>
>The indentation shown in this section was solely for purposes of clarity. You do not have to indent the rules found inside an @media block, but you’re welcome to do so if it makes your CSS easier for you to read.</Tips>
>As of this writing, a couple of browsers also support projection, which allows a document to be presented as a slideshow. Several mobile-device browsers support the handheld type, but not in consistent ways.</Tips>
>
>
>
>
>
> 在任何情况下，即使其中一个媒体查询的结果是“true”，也会应用相关联的样式表。因此，给定前面的@import，如果将其呈现到彩色打印机或彩色屏幕环境中，将应用 print-color.css。如果在黑白打印机上打印，两个查询都将计算为“false”，并且 print-color.css 将不应用于文档。这同样适用于任何屏幕媒体，等等。
> 每个媒体描述符由一个媒体类型和一个或多个列出的媒体特性组成，每个媒体特性描述符括在括号中。如果没有提供媒体类型，则假设为 all，这使得下面两个例子等价:
> 一般来说，媒体特性描述符的格式类似于 CSS 中的属性-值对。有一些不同之处，最明显的是一些特性可以在没有附加值的情况下指定。因此，例如，任何基于颜色的媒体将使用(color)进行匹配，而任何使用 16 位颜色深度的媒体将使用(color: 16)进行匹配。实际上，使用没有值的描述符是对描述符的真/假测试:(颜色)表示“该媒体是彩色的吗?”
> 多个特征描述符可以与 and logical 关键字链接。事实上，在媒体查询中有两个逻辑关键字:
> 将两个或多个媒体特性链接在一起，使所有特性都为真，查询才为真。例如，(color)和(朝向:landscape)和(min-device-width: 800px)意味着必须满足所有三个条件:如果媒体环境有颜色，处于横向方向，并且设备的显示宽度至少为 800 像素，则使用样式表。
> 否定整个查询，如果所有条件都为真，则不应用样式表。例如，not (color)和(orientation: landscape)和(min-device-width: 800px)表示如果满足这三个条件，则语句被否定。因此，如果媒体环境有颜色，是横向的，并且设备的显示宽度至少为 800 像素，那么样式表将不被使用。在所有其他情况下，都将使用它。
> 注意，not 关键字只能在媒体查询的开头使用。像(color)和(min-device-width: 800px)这样的代码是不合法的。在这种情况下，查询将被忽略。还要注意的是，那些太老而不能理解媒体查询的浏览器总是会跳过一个以 not 开头的样式表。没有用于媒体查询的 OR 关键字。相反，分隔查询列表的逗号具有 or - screen 的功能，print 表示“如果媒体是 screen 或 print，则应用”。你应该写 screen 和(max-color: 2)或(monochrome)，而不是 screen 和(max-color: 2)或(monochrome)，这是无效的，因此被忽略了。
> 还有一个关键字 only，它被设计成故意向后不兼容(是的，真的):
>`
>`
> 这基本上相当于写以下内容:
> 但是，除了“和”操作之外，还有更多可用的操作。CSS 形状(在第 10 章中详细介绍)是一个很好的例子，说明为什么“或”是有用的，因为长期以来 WebKit 只通过供应商前缀属性支持 CSS 形状。因此，如果你想使用形状，你可以使用这样的功能查询:
> 您仍然需要确保同时使用带前缀和不带前缀的形状属性，但是这将允许您在 WebKit 发布行中向后添加对这些属性的支持，同时支持其他也支持形状的浏览器，但不是通过带前缀的属性。
> 所有这些都非常方便，因为在某些情况下，您可能希望应用不同于测试的属性。因此，要回到网格布局，您可能需要在使用网格时更改布局元素的页边距等。下面是这种方法的一个简化版本:
> 也可以使用否定。例如，你可以在不支持网格布局的情况下应用以下样式:
> 您可以将逻辑运算符组合成单个查询，但是需要使用括号来保持逻辑的正确性。假设我们希望在支持颜色时应用一组样式，在支持网格或灵活的框布局时应用一组样式。它是这样写的:
> 请注意，在逻辑的“或”部分周围还有一组括号，用于封装网格和 flex 测试。需要那些额外的括号。没有它们，整个表达式将失败，块内的样式将被跳过。换句话说，不要这样做:
> 最后，您可能想知道为什么特性查询测试需要属性和值。毕竟，如果你使用的是形状，你需要测试的只是外形，对吧?这是因为浏览器可以很容易地支持一个属性，而不需要支持它的所有值。网格布局就是一个完美的例子。假设你可以像这样测试网格支持:
> 甚至 Internet Explorer 4 也支持显示。任何理解@supports 的浏览器肯定都能理解 display 和它的许多值——但可能不是 grid。这就是为什么属性和值总是在特性查询中测试的原因。
>Remember that these are feature queries, not correctness queries. A browser can understand the feature you’re testing for, but implement it with bugs. So you’re not getting an assurance from the browser that it supports something correctly. All a positive featurequery result means is that the browser understands what you’ve said and makes some sort of attempt to support it.</Tips>
> 使用 CSS，完全改变用户代理显示元素的方式是可能的。这可以通过 display 属性在基本级别上执行，也可以通过将样式表与文档关联的不同方式执行。用户永远不会知道这是通过外部样式表还是嵌入式样式表，甚至是内联样式表来完成的。外部样式表的真正重要性在于，它允许作者将站点的所有表示信息放在一个地方，并将所有文档指向那个地方。这不仅使站点更新和维护变得轻而易举，而且还有助于节省带宽，因为所有的表示都从文档中删除了。使用@supports()，甚至可以在原生 CSS 中进行一些基本的渐进式增强。
> 为了充分利用 CSS 的强大功能，作者需要知道如何将一组样式与文档中的元素关联起来。要完全理解 CSS 是如何做到这一切的，作者需要掌握 CSS 选择文档片段进行样式化的方法，这是下一章的主题。