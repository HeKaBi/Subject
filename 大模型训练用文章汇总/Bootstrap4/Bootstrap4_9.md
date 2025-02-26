## Bootstrap4 信息提示框

Bootstrap 4 可以很容易实现信息提示框。

![](https://www.runoob.com/wp-content/uploads/2017/10/06CC7655-91D9-4953-A8CC-33F50A21404E.jpg)

提示框可以使用 .alert 类, 后面加上 .alert-success, .alert-info, .alert-warning, .alert-danger, .alert-primary, .alert-secondary, .alert-light 或 .alert-dark 类来实现:

## 实例

<div class\="alert alert-success"\> <strong\>成功!</strong\> 指定操作成功提示信息。 </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_alerts)

* * *

## 提示框添加链接

提示框中在链接的标签上添加 alert-link 类来设置匹配提示框颜色的链接：

## 实例

<div class\="alert alert-success"\> <strong\>成功!</strong\> 你应该认真阅读 <a href\="#" class\="alert-link"\>这条信息</a\>。 </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_alerts_link)

* * *

## 关闭提示框

我们可以在提示框中的 div 中添加 .alert-dismissible 类，然后在关闭按钮的链接上添加 class="close" 和 data-dismiss="alert" 类来设置提示框的关闭操作。

## 实例

<div class\="alert alert-success alert-dismissible"\> <button type\="button" class\="close" data-dismiss\="alert"\>&times;</button\> <strong\>成功!</strong\> 指定操作成功提示信息。 </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_alerts_dismissible)

**提示:** &times; (×) 是 HTML 实体字符，来表示关闭操作，而不是字母 "x"。

* * *

## 提示框动画

.fade 和 .show 类用于设置提示框在关闭时的淡出和淡入效果：

## 实例

<div class\="alert alert-danger alert-dismissible fade show"\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_alerts_fade)