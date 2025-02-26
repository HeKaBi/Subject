## HTML DOM - 修改 HTML 内容

* * *

通过 HTML DOM，JavaScript 能够访问 HTML 文档中的每个元素。  

* * *

## 改变 HTML 内容

改变元素内容的最简单的方法是使用 innerHTML 属性。

下面的例子更改 <p> 元素的 HTML 内容：

## 实例

<p id\="p1"\>Hello World!</p\> <script\> document.getElementById("p1").innerHTML="新文本!"; </script\> <p\>段落通过脚本来修改内容。</p\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_changetext)

  

* * *

## 改变 HTML 样式

通过 HTML DOM，您能够访问 HTML 对象的样式对象。

下面的例子更改段落的 HTML 样式：

## 实例

<p id\="p1"\>Hello world!</p\> <p id\="p2"\>Hello world!</p\> <script\> document.getElementById("p2").style.color="blue"; document.getElementById("p2").style.fontFamily="Arial"; document.getElementById("p2").style.fontSize="larger"; </script\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_changestyle1)

  

* * *

## 使用事件

HTML DOM 允许您在事件发生时执行代码。

当 HTML 元素"有事情发生"时，浏览器就会生成事件：

+   在元素上点击
+   加载页面
+   改变输入字段

你可以在下一章学习更多有关事件的内容。

下面两个例子在按钮被点击时改变 <body> 元素的背景色：

## 实例

<input type\="button" onclick\="document.body.style.backgroundColor='lavender';" value\="修改背景颜色"\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_changebackground2)

在本例中，由函数执行相同的代码：

## 实例

<script\> function ChangeBackground() { document.body.style.backgroundColor="lavender"; } </script\> <input type\="button" onclick\="ChangeBackground()" value\="修改背景颜色" />

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_changestyle)

下面的例子在按钮被点击时改变 <p> 元素的文本：

## 实例

<p id\="p1"\>Hello world!</p\> <script\> function ChangeText() { document.getElementById("p1").innerHTML="Hello Runoob!"; } </script\> <input type\="button" onclick\="ChangeText()" value\="修改文本" />

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_changetext2)