## HTML DOM 方法

* * *

HTML DOM 方法是我们可以在节点（HTML 元素）上执行的动作。

HTML DOM 属性是我们可以在节点（HTML 元素）设置和修改的值。

* * *

## 编程接口

可通过 JavaScript （以及其他编程语言）对 HTML DOM 进行访问。

所有 HTML 元素被定义为对象，而编程接口则是对象方法和对象属性。

方法是您能够执行的动作（比如添加或修改元素）。

属性是您能够获取或设置的值（比如节点的名称或内容）。

* * *

## getElementById() 方法

getElementById() 方法返回带有指定 ID 的元素：

## 实例

var element\=document.getElementById("intro");

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_getelementbyid)

  

* * *

## HTML DOM 对象 - 方法和属性

一些常用的 HTML DOM 方法：

+   getElementById(id) - 获取带有指定 id 的节点（元素）
+   appendChild(node) - 插入新的子节点（元素）
+   removeChild(node) - 删除子节点（元素）

一些常用的 HTML DOM 属性：

+   innerHTML - 节点（元素）的文本值
+   parentNode - 节点（元素）的父节点
+   childNodes - 节点（元素）的子节点
+   attributes - 节点（元素）的属性节点

您将在本教程的下一章中学到更多有关属性的知识。

* * *

## 现实生活中的对象

某个人是一个对象。

人的方法可能是 eat(), sleep(), work(), play() 等等。

所有人都有这些方法，但会在不同时间执行它们。

一个人的属性包括姓名、身高、体重、年龄、性别等等。

所有人都有这些属性，但它们的值因人而异。

* * *

## 一些 DOM 对象方法

这里提供一些您将在本教程中学到的常用方法：

| 方法                     | 描述                                                         |
| ------------------------ | ------------------------------------------------------------ |
| getElementById()         | 返回带有指定 ID 的元素。                                     |
| getElementsByTagName()   | 返回包含带有指定标签名称的所有元素的节点列表（集合/节点数组）。 |
| getElementsByClassName() | 返回包含带有指定类名的所有元素的节点列表。                   |
| appendChild()            | 把新的子节点添加到指定节点。                                 |
| removeChild()            | 删除子节点。                                                 |
| replaceChild()           | 替换子节点。                                                 |
| insertBefore()           | 在指定的子节点前面插入新的子节点。                           |
| createAttribute()        | 创建属性节点。                                               |
| createElement()          | 创建元素节点。                                               |
| createTextNode()         | 创建文本节点。                                               |
| getAttribute()           | 返回指定的属性值。                                           |
| setAttribute()           | 把指定属性设置或修改为指定的值。                             |