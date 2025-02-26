## HTML DOM 导航

* * *

通过 HTML DOM，您能够使用节点关系在节点树中导航。

* * *

## HTML DOM 节点列表

getElementsByTagName() 方法返回*节点列表*。节点列表是一个节点数组。

下面的代码选取文档中的所有 <p> 节点：

## 实例

var x\=document.getElementsByTagName("p");

可以通过下标号访问这些节点。如需访问第二个 <p>，您可以这么写：

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_nodelist)

**注意：**

下标号从 0 开始。

* * *

## HTML DOM 节点列表长度

length 属性定义节点列表中节点的数量。

您可以使用 length 属性来循环节点列表：

## 实例

x\=document.getElementsByTagName("p"); for (i\=0;i<x.length;i++) { document.write(x\[i\].innerHTML); document.write("<br>"); }

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_nodelist_length)

### 实例解析：

+   获取所有 <p> 元素节点
+   输出每个 <p> 元素的文本节点的值

* * *

## 导航节点关系

您能够使用三个节点属性：parentNode、firstChild 以及 lastChild ，在文档结构中进行导航。

请看下面的 HTML 片段：

<html\> <head\> <meta charset\="utf-8"\> </head\> <body\> <p\>Hello World!</p\> <div\> <p\>DOM 是非常有用的!</p\> <p\>这个实例演示了节点的关系。</p\> </div\> </body\> </html\>

+   首个 <p> 元素是 <body> 元素的首个子元素（firstChild）
+   <div> 元素是 <body> 元素的最后一个子元素（lastChild）
+   <body> 元素是首个 <p> 元素和 <div> 元素的父节点（parentNode）

firstChild 属性可用于访问元素的文本：

## 实例

<p id\="intro"\>Hello World!</p\> <script\> x=document.getElementById("intro"); document.write(x.firstChild.nodeValue); </script\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_firstchild)

  

* * *

## DOM 根节点

这里有两个特殊的属性，可以访问全部文档：

+   document.documentElement - 全部文档
+   document.body - 文档的主体

## 实例

<p\>Hello World!</p\> <div\> <p\>DOM 是非常有用的!</p\> <p\>这个实例演示了 <b\>document.body</b\> 属性。</p\> </div\> <script\> alert(document.body.innerHTML); </script\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_root)

  

* * *

## childNodes 和 nodeValue

除了 innerHTML 属性，您也可以使用 childNodes 和 nodeValue 属性来获取元素的内容。

下面的代码获取 id="intro" 的 <p> 元素的值：

## 实例

<p id\="intro"\>Hello World!</p\> <script\> txt=document.getElementById("intro").childNodes\[0\].nodeValue; document.write(txt); </script\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_methods2)

在上面的例子中，getElementById 是一个方法，而 childNodes 和 nodeValue 是属性。

在本教程中，我们将使用 innerHTML 属性。不过，学习上面的方法有助于对 DOM 树结构和导航的理解。