## Bootstrap4 表单

在本章中，我们将学习如何使用 Bootstrap 创建表单。Bootstrap 通过一些简单的 HTML 标签和扩展的类即可创建出不同样式的表单。

表单元素 <input>, <textarea>, 和 <select> elements 在使用 .form-control 类的情况下，宽度都是设置为 100%。

### Bootstrap4 表单布局

+   堆叠表单 (全屏宽度)：垂直方向
+   内联表单：水平方向

Bootstrap 提供了两种类型的表单布局:

* * *

## 堆叠表单

以下实例使用两个输入框，一个复选框，一个提交按钮来创建堆叠表单：

## 实例

<form action\=""\> <div class\="form-group"\> <label for\="email"\>Email address:</label\> <input type\="email" class\="form-control" placeholder\="Enter email" id\="email"\> </div\> <div class\="form-group"\> <label for\="pwd"\>Password:</label\> <input type\="password" class\="form-control" placeholder\="Enter password" id\="pwd"\> </div\> <div class\="form-group form-check"\> <label class\="form-check-label"\> <input class\="form-check-input" type\="checkbox"\> Remember me </label\> </div\> <button type\="submit" class\="btn btn-primary"\>Submit</button\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_basic)

显示效果：

![](https://www.runoob.com/wp-content/uploads/2017/10/BE33BCD9-4AE4-4349-B4FD-BEC4D7669670.jpg)

* * *

## 内联表单

所有内联表单中的元素都是左对齐的。

**注意：在屏幕宽度小于 576px 时为垂直堆叠，如果屏幕宽度大于等于576px时表单元素才会显示在同一个水平线上。**

内联表单需要在 <form> 元素上添加 .form-inline类。

以下实例使用两个输入框，一个复选框，一个提交按钮来创建内联表单：

## 实例

<form class\="form-inline"\> <label for\="email"\>Email address:</label\> <input type\="email" class\="form-control" id\="email"\> <label for\="pwd"\>Password:</label\> <input type\="password" class\="form-control" id\="pwd"\> <div class\="form-check"\> <label class\="form-check-label"\> <input class\="form-check-input" type\="checkbox"\> Remember me </label\> </div\> <button type\="submit" class\="btn btn-primary"\>Submit</button\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_inline)

显示效果：

![](https://www.runoob.com/wp-content/uploads/2017/10/CBA259C0-910B-416D-9347-E7541E0AD003.jpg)

上面的实例元素排列看起来很紧凑，可以使用 .mr-sm-2 类来设置右边距，使用.mb-2 类设置底部边距：

## 实例

<form class\="form-inline" action\=""\> <label for\="email" class\="mr-sm-2"\>Email address:</label\> <input type\="email" class\="form-control mb-2 mr-sm-2" placeholder\="Enter email" id\="email"\> <label for\="pwd" class\="mr-sm-2"\>Password:</label\> <input type\="password" class\="form-control mb-2 mr-sm-2" placeholder\="Enter password" id\="pwd"\> <div class\="form-check mb-2 mr-sm-2"\> <label class\="form-check-label"\> <input class\="form-check-input" type\="checkbox"\> Remember me </label\> </div\> <button type\="submit" class\="btn btn-primary mb-2"\>Submit</button\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_inline2)

显示效果：

![](https://www.runoob.com/wp-content/uploads/2017/10/ACF6334D-2B27-41B2-A4DB-6768065840AE.jpg)

## 表单行/网格

我们还可以使用 .col 类来控制表单元素的宽度和对齐方式，不需要使用间距类。 .col 类来控制的表单需要放在 .row 容器中。

以下实例将两个列并排显示：

## 实例

<form\> <div class\="row"\> <div class\="col"\> <input type\="text" class\="form-control" id\="email" placeholder\="Enter email" name\="email"\> </div\> <div class\="col"\> <input type\="password" class\="form-control" placeholder\="Enter password" name\="pswd"\> </div\> </div\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_grid)

显示效果：

![](https://www.runoob.com/wp-content/uploads/2017/10/AB67AA60-CE57-4514-8BB2-2929DADCF47D.jpg)

如果网格要使用比较小的间距可以使用 .form-row 替代 .row:

## 实例

<form\> <div class\="form-row"\> <div class\="col"\> <input type\="text" class\="form-control" id\="email" placeholder\="Enter email" name\="email"\> </div\> <div class\="col"\> <input type\="password" class\="form-control" placeholder\="Enter password" name\="pswd"\> </div\> </div\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_grid2)

* * *

## 表单验证

我们可以使用不同的验证类来设置表单的验证功能。

.was-validated 或 .needs-validation 添加到 <form> 元素中，input 输入字段将具有绿色（有效）或红色（无效）边框效果，用于说明表单是否需要输入内容。

.valid-feedback 或 .invalid-feedback 类用来告诉用户缺少什么信息，或者在提交表单之前需要完成什么。

## 实例

使用 .was-validated 类显示表单在提交之前需要填写的内容：

<form action\="" class\="was-validated"\> <div class\="form-group"\> <label for\="uname"\>Username:</label\> <input type\="text" class\="form-control" id\="uname" placeholder\="Enter username" name\="uname" required\> <div class\="valid-feedback"\>验证成功！</div\> <div class\="invalid-feedback"\>请输入用户名！</div\> </div\> <div class\="form-group"\> <label for\="pwd"\>Password:</label\> <input type\="password" class\="form-control" id\="pwd" placeholder\="Enter password" name\="pswd" required\> <div class\="valid-feedback"\>验证成功！</div\> <div class\="invalid-feedback"\>请输入密码！</div\> </div\> <div class\="form-group form-check"\> <label class\="form-check-label"\> <input class\="form-check-input" type\="checkbox" name\="remember" required\> 同意协议 <div class\="valid-feedback"\>验证成功！</div\> <div class\="invalid-feedback"\>同意协议才能提交。</div\> </label\> </div\> <button type\="submit" class\="btn btn-primary"\>提交</button\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs_form_validation_was)

## 实例

使用 .needs-validation，它将在表单提交之后验证缺少的内容。这里需要添加一些 JavaScript 代码才能使代码正常工作：

<form action\="" class\="needs-validation" novalidate\> <div class\="form-group"\> <label for\="uname"\>Username:</label\> <input type\="text" class\="form-control" id\="uname" placeholder\="Enter username" name\="uname" required\> <div class\="valid-feedback"\>验证成功！</div\> <div class\="invalid-feedback"\>请输入用户名！</div\> </div\> <div class\="form-group"\> <label for\="pwd"\>Password:</label\> <input type\="password" class\="form-control" id\="pwd" placeholder\="Enter password" name\="pswd" required\> <div class\="valid-feedback"\>验证成功！</div\> <div class\="invalid-feedback"\>请输入密码！</div\> </div\> <div class\="form-group form-check"\> <label class\="form-check-label"\> <input class\="form-check-input" type\="checkbox" name\="remember" required\> 同意协议 <div class\="valid-feedback"\>验证成功！</div\> <div class\="invalid-feedback"\>同意协议才能提交。</div\> </label\> </div\> <button type\="submit" class\="btn btn-primary"\>提交</button\> </form\> <script\> // 如果验证不通过禁止提交表单 (function() { 'use strict'; window.addEventListener('load', function() { // 获取表单验证样式 var forms = document.getElementsByClassName('needs-validation'); // 循环并禁止提交 var validation = Array.prototype.filter.call(forms, function(form) { form.addEventListener('submit', function(event) { if (form.checkValidity() === false) { event.preventDefault(); event.stopPropagation(); } form.classList.add('was-validated'); }, false); }); }, false); })(); </script\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs_form_validation_needs)