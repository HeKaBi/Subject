## HTML DOM 属性

* * *

属性是节点（HTML 元素）的值，您能够获取或设置。

* * *

## 编程接口

可通过 JavaScript （以及其他编程语言）对 HTML DOM 进行访问。

所有 HTML 元素被定义为对象，而编程接口则是对象方法和对象属性。

方法是您能够执行的动作（比如添加或修改元素）。

属性是您能够获取或设置的值（比如节点的名称或内容）。

* * *

## innerHTML 属性

获取元素内容的最简单方法是使用 innerHTML 属性。

innerHTML 属性对于获取或替换 HTML 元素的内容很有用。

## 实例

下面的代码获取 id="intro" 的 <p> 元素的 innerHTML：

## 实例

<!DOCTYPE html\> <html\> <head\> <meta charset\="utf-8"\> </head\> <body\> <p id\="intro"\>Hello World!</p\> <script\> var txt=document.getElementById("intro").innerHTML; document.write(txt); </script\> </body\> </html\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_methods)

在上面的例子中，getElementById 是一个方法，而 innerHTML 是属性。

<table class="lamp"><tbody><tr><th><img decoding="async" src="https://www.runoob.com/images/lamp.jpg" width="32" height="32" alt="lamp"></th><td><p>innerHTML 属性可用于获取或改变任意 HTML 元素，包括 &lt;html&gt; 和 &lt;body&gt;。</p></td></tr></tbody></table>

  

* * *

nodeName 属性规定节点的名称。

+   nodeName 是只读的
+   元素节点的 nodeName 与标签名相同
+   属性节点的 nodeName 与属性名相同
+   文本节点的 nodeName 始终是 #text
+   文档节点的 nodeName 始终是 #document

**注意：** nodeName 始终包含 HTML 元素的大写字母标签名。

* * *

## nodeValue 属性

nodeValue 属性规定节点的值。

+   元素节点的 nodeValue 是 undefined 或 null
+   文本节点的 nodeValue 是文本本身
+   属性节点的 nodeValue 是属性值

* * *

## 获取元素的值

下面的例子会取回 <p id="intro"> 标签的文本节点值：

## 实例

<!DOCTYPE html\> <html\> <head\> <meta charset\="utf-8"\> </head\> <body\> <p id\="intro"\>Hello World!</p\> <script\> x=document.getElementById("intro"); document.write(x.firstChild.nodeValue); </script\> </body\> </html\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_firstchild)

  

* * *

## nodeType 属性

nodeType 属性返回节点的类型。nodeType 是只读的。

比较重要的节点类型有：

| 元素类型 | NodeType |
| -------- | -------- |
| 元素     | 1        |
| 属性     | 2        |
| 文本     | 3        |
| 注释     | 8        |
| 文档     | 9        |