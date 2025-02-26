## Bootstrap4 面包屑导航（Breadcrumb）

面包屑导航是一种基于网站层次信息的显示方式。以博客为例，面包屑导航可以显示发布日期、类别或标签。它们表示当前页面在导航层次结构内的位置，是在用户界面中的一种导航辅助。

Bootstrap 中的面包屑导航是一个简单的带有 **.breadcrumb** class 的无序列表。分隔符会通过 CSS（bootstrap.min.css）中的 ::before 和 content 来添加，下面所示的 class 自动被添加：

```
.breadcrumb-item + .breadcrumb-item::before {
  display: inline-block;
  padding-right: 0.5rem;
  color: #6c757d;
  content: "/";
}
```

## Bootstrap4 面包屑导航实例

<ol class\="breadcrumb"\> <li class\="breadcrumb-item active"\>Home</li\> </ol\> <ol class\="breadcrumb"\> <li class\="breadcrumb-item"\><a href\="#"\>Home</a\></li\> <li class\="breadcrumb-item active"\>Library</li\> </ol\> <ol class\="breadcrumb"\> <li class\="breadcrumb-item"\><a href\="#"\>Home</a\></li\> <li class\="breadcrumb-item"\><a href\="#"\>Library</a\></li\> <li class\="breadcrumb-item active"\>Data</li\> </ol\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_breadcrumb)

我们也可以不用列表形式：

## Bootstrap4 面包屑导航实例

<nav class\="breadcrumb"\> <a class\="breadcrumb-item" href\="#"\>Home</a\> <a class\="breadcrumb-item" href\="#"\>Library</a\> <a class\="breadcrumb-item" href\="#"\>Data</a\> <span class\="breadcrumb-item active"\>Bootstrap</span\> </nav\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_breadcrumb2)