## HTML DOM 访问

* * *

访问 HTML DOM - 查找 HTML 元素。

* * *

## 访问 HTML 元素（节点）

访问 HTML 元素等同于访问节点

您能够以不同的方式来访问 HTML 元素：

+   通过使用 getElementById() 方法
+   通过使用 getElementsByTagName() 方法
+   通过使用 getElementsByClassName() 方法

* * *

## getElementById() 方法

getElementById() 方法返回带有指定 ID 的元素引用：

### 语法

*node*.getElementById(*"id"*);

下面的例子获取 id="intro" 的元素：

## 实例

document.getElementById("intro");

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_getelementbyid)

  

* * *

## getElementsByTagName() 方法

getElementsByTagName() 返回带有指定标签名的所有元素。

### 语法

*node*.getElementsByTagName(*"tagname"*);

下面的例子返回包含文档中所有 <p> 元素的列表：

## 实例 1

document.getElementsByTagName("p");

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_getelementsbytagname)

下面的例子返回包含文档中所有 <p> 元素的列表，并且这些 <p> 元素应该是 id="main" 的元素的后代（子、孙等等）：

## 实例 2

document.getElementById("main").getElementsByTagName("p");

[尝试一下 »](https://www.runoob.com/try/try.php?filename=try_getelementsbytagname2)

  

* * *

## The getElementsByClassName() Method

如果您希望查找带有相同类名的所有 HTML 元素，请使用这个方法：

document.getElementsByClassName("intro");

上面的例子返回包含 class="intro" 的所有元素的一个列表：

**注意：**getElementsByClassName() 在 Internet Explorer 5,6,7,8 中无效。