## HTML DOM - 事件

* * *

HTML DOM 允许 JavaScript 对 HTML 事件作出反应。

## 实例

  

* * *

## 对事件作出反应

当事件发生时，可以执行 JavaScript，比如当用户点击一个 HTML 元素时。

如需在用户点击某个元素时执行代码，请把 JavaScript 代码添加到 HTML 事件属性中：

HTML 事件的例子：

+   当用户点击鼠标时
+   当网页已加载时
+   当图片已加载时
+   当鼠标移动到元素上时
+   当输入字段被改变时
+   当 HTML 表单被提交时
+   当用户触发按键时

在本例中，当用户点击时，会改变 <h1> 元素的内容：

## 实例

<h1 onclick\="this.innerHTML='Ooops!'"\>点击文本!</h1\>

[尝试一下 »](https://www.runoob.com/try/tryit.php?filename=trydhtml_event_onclick2)

在本例中，会从事件处理程序中调用函数：

## 实例

<script\> function changetext(id){ id.innerHTML="Ooops!"; } </script\> </head\> <body\> <h1 onclick\="changetext(this)"\>点击文本!</h1\>

[尝试一下 »](https://www.runoob.com/try/tryit.php?filename=trydhtml_event_onclick3)

  

* * *

## HTML 事件属性

如需向 HTML 元素分配事件，您可以使用事件属性。

## 实例

向 button 元素分配一个 onclick 事件：

<button onclick\="displayDate()"\>点我</button\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=tryhtmldom_events1)

在上面的例子中，当点击按钮时，会执行名为 displayDate 的函数。

* * *

## 使用 HTML DOM 来分配事件

HTML DOM 允许您使用 JavaScript 向 HTML 元素分配事件：

## 实例

为 button 元素分配 onclick 事件：

document.getElementById("myBtn").onclick\=function(){displayDate()};

[尝试一下 »](https://www.runoob.com/try/try.php?filename=tryhtmldom_events2)

在上面的例子中，名为 displayDate 的函数被分配给了 id=myButn" 的 HTML 元素。

当按钮被点击时，将执行函数。

* * *

## onload 和 onunload 事件

当用户进入或离开页面时，会触发 onload 和 onunload 事件。

onload 事件可用于检查访客的浏览器类型和版本，以便基于这些信息来加载不同版本的网页。

onload 和 onunload 事件可用于处理 cookies。

## 实例

<body onload\="checkCookies()"\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=tryhtmldom_events_onload)

  

* * *

## onchange 事件

onchange 事件常用于输入字段的验证。

下面的例子展示了如何使用 onchange。当用户改变输入字段的内容时，将调用 upperCase() 函数。

## 实例

<input type\="text" id\="fname" onchange\="upperCase()"\>

[尝试一下 »](https://www.runoob.com/try/tryit.php?filename=tryjsref_onchange)

  

* * *

## onmouseover 和 onmouseout 事件

onmouseover 和 onmouseout 事件可用于在鼠标指针移动到或离开元素时触发函数。

## 实例

一个简单的 onmouseover-onmouseout 实例:

[尝试一下 »](https://www.runoob.com/try/try.php?filename=tryhtmldom_events_mouseover)

  

* * *

## onmousedown、onmouseup 以及 onclick 事件

onmousedown、onmouseup 以及 onclick 事件是鼠标点击的全部过程。首先当某个鼠标按钮被点击时，触发 onmousedown 事件，然后，当鼠标按钮被松开时，会触发 onmouseup 事件，最后，当鼠标点击完成时，触发 onclick 事件。

## 实例

一个简单的 onmousedown-onmouseup 实例：

[尝试一下 »](https://www.runoob.com/try/try.php?filename=tryhtmldom_events_mousedown)

  

* * *

## HTML DOM 事件对象参考手册

如需每个事件的完整描述和例子，请访问我们的 [HTML DOM 参考手册](https://www.runoob.com/jsref/jsref-tutorial.html)。