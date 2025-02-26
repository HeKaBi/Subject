## HTML DOM - 元素

* * *

添加、删除和替换 HTML 元素。

* * *

## 创建新的 HTML 元素 - createElement()

如需向 HTML DOM 添加新元素，您首先必须创建该元素，然后把它追加到已有的元素上。

##  实例

<div id\="div1"\> <p id\="p1"\>这是一个段落。</p\> <p id\="p2"\>这是另一个段落。</p\> </div\> <script\> var para=document.createElement("p"); var node=document.createTextNode("这是一个新段落。"); para.appendChild(node); var element=document.getElementById("div1"); element.appendChild(para); </script\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_elementcreate)

  

* * *

## 实例解析

这段代码创建了一个新的 <p> 元素：

var para=document.createElement("p");

如需向 <p> 元素添加文本，您首先必须创建文本节点。这段代码创建文本节点：

var node=document.createTextNode("这是一个新段落。");

然后您必须向 <p> 元素追加文本节点：

最后，您必须向已有元素追加这个新元素。

这段代码查找到一个已有的元素：

var element=document.getElementById("div1");

这段代码向这个已存在的元素追加新元素：

element.appendChild(para);

  

* * *

## 创建新的 HTML 元素 - insertBefore()

上一个例子中的 appendChild() 方法，将新元素作为父元素的最后一个子元素进行添加。

如果不希望如此，您可以使用 insertBefore() 方法：

##  实例

<div id\="div1"\> <p id\="p1"\>这是一个段落。</p\> <p id\="p2"\>这是另外一个段落。</p\> </div\> <script\> var para=document.createElement("p"); var node=document.createTextNode("这是一个新段落。"); para.appendChild(node); var element=document.getElementById("div1"); var child=document.getElementById("p1"); element.insertBefore(para,child); </script\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_elementcreate2)

  

* * *

## 删除已有的 HTML 元素

如需删除 HTML 元素，您必须清楚该元素的父元素：

## 实例

<div id\="div1"\> <p id\="p1"\>这是一个段落。</p\> <p id\="p2"\>这是另一个段落。</p\> </div\> <script\> var parent=document.getElementById("div1"); var child=document.getElementById("p1"); parent.removeChild(child); </script\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_elementremove)

  

* * *

## 实例解析

这个 HTML 文档包含一个带有两个子节点（两个 <p> 元素）的 <div> 元素：

<div id="div1">  
<p id="p1">这是一个段落。</p>  
<p id="p2">这是另一个段落。</p>  
</div>

查找 id="div1" 的元素：

var parent=document.getElementById("div1");

查找 id="p1" 的 <p> 元素：

var child=document.getElementById("p1");

从父元素中删除子元素：

parent.removeChild(child);

  

<table class="lamp"><tbody><tr><th><img decoding="async" src="https://www.runoob.com/images/lamp.jpg" width="32" height="32" alt="lamp"></th><td>能否在不引用父元素的情况下删除某个元素？<br>很抱歉。DOM 需要了解您需要删除的元素，以及它的父元素。</td></tr></tbody></table>

这里提供一个常用的解决方法：找到您需要删除的子元素，然后使用 parentNode 属性来查找其父元素：

var child=document.getElementById("p1");  
child.parentNode.removeChild(child);

  

* * *

## 替换 HTML 元素

如需替换 HTML DOM 中的元素，请使用 replaceChild() 方法：

## 实例

<div id\="div1"\> <p id\="p1"\>这是一个段落。</p\> <p id\="p2"\>这是另外一个段落。</p\> </div\> <script\> var parent=document.getElementById("div1"); var child=document.getElementById("p1"); var para=document.createElement("p"); var node=document.createTextNode("这是一个新的段落。"); para.appendChild(node); parent.replaceChild(para,child); </script\>
[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_elementreplace)