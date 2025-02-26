## Bootstrap4 表单控件

Bootstrap4 支持以下表单控件：

+   input
+   textarea
+   checkbox
+   radio
+   select

## Bootstrap Input

Bootstrap 支持所有的 HTML5 输入类型: text, password, datetime, datetime-local, date, month, time, week, number, email, url, search, tel, 以及 color。

**注意：:** 如果 input 的 type 属性未正确声明，输入框的样式将不会显示。

以下实例使用两个 input 元素，一个是 text，一个是 password ：

## 实例

<div class\="form-group"\> <label for\="usr"\>用户名:</label\> <input type\="text" class\="form-control" id\="usr"\> </div\> <div class\="form-group"\> <label for\="pwd"\>密码:</label\> <input type\="password" class\="form-control" id\="pwd"\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_form_input)

* * *

## Bootstrap textarea

以下实例演示了 textarea 的样式。

## 实例

<div class\="form-group"\> <label for\="comment"\>评论:</label\> <textarea class\="form-control" rows\="5" id\="comment"\></textarea\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_form_textarea)

* * *

## Bootstrap 复选框(checkbox)

复选框用于让用户从一系列预设置的选项中进行选择，可以选一个或多个。

以下实例包含了三个选项。最后一个是禁用的：

## 实例

<div class\="form-check"\> <label class\="form-check-label"\> <input type\="checkbox" class\="form-check-input" value\=""\>Option 1 </label\> </div\> <div class\="form-check"\> <label class\="form-check-label"\> <input type\="checkbox" class\="form-check-input" value\=""\>Option 2 </label\> </div\> <div class\="form-check disabled"\> <label class\="form-check-label"\> <input type\="checkbox" class\="form-check-input" value\="" disabled\>Option 3 </label\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_form_checkbox)

使用 .form-check-inline 类可以让选项显示在同一行上：

## 实例

<div class\="form-check form-check-inline"\> <label class\="form-check-label"\> <input type\="checkbox" class\="form-check-input" value\=""\>Option 1 </label\> </div\> <div class\="form-check form-check-inline"\> <label class\="form-check-label"\> <input type\="checkbox" class\="form-check-input" value\=""\>Option 2 </label\> </div\> <div class\="form-check form-check-inline disabled"\> <label class\="form-check-label"\> <input type\="checkbox" class\="form-check-input" value\="" disabled\>Option 3 </label\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_form_checkbox_inline)

* * *

## Bootstrap 单选框(Radio)

单选框用于让用户从一系列预设置的选项中进行选择，只能选一个。

以下实例包含了三个选项。最后一个是禁用的：

## 实例

<div class\="radio"\> <label\><input type\="radio" name\="optradio"\>Option 1</label\> </div\> <div class\="radio"\> <label\><input type\="radio" name\="optradio"\>Option 2</label\> </div\> <div class\="radio disabled"\> <label\><input type\="radio" name\="optradio" disabled\>Option 3</label\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_form_radio)

使用 .radio-inline 类可以让选项显示在同一行上：

## 实例

<label class\="radio-inline"\><input type\="radio" name\="optradio"\>Option 1</label\> <label class\="radio-inline"\><input type\="radio" name\="optradio"\>Option 2</label\> <label class\="radio-inline"\><input type\="radio" name\="optradio" disabled\>Option 3</label\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_form_radio_inline)

* * *

## Bootstrap select 下拉菜单

当您想让用户从多个选项中进行选择，但是默认情况下只能选择一个选项时，则使用选择框。

以下实例包含了两个下拉菜单：

## 实例

<div class\="form-group"\> <label for\="sel1"\>下拉菜单:</label\> <select class\="form-control" id\="sel1"\> <option\>1</option\> <option\>2</option\> <option\>3</option\> <option\>4</option\> </select\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_form_select)