## Bootstrap4 输入框组

我们可以使用 .input-group 类来向表单输入框中添加更多的样式，如图标、文本或者按钮。

使用 .input-group-prepend 类可以在输入框的的前面添加文本信息， .input-group-append 类添加在输入框的后面。

最后，我们还需要使用 .input-group-text 类来设置文本的样式。

![](https://www.runoob.com/wp-content/uploads/2018/06/F42CE8CE-7FFF-4979-B1DA-6A03015C0A77.png)

## Bootstrap4 实例

<form\> <div class\="input-group mb-3"\> <div class\="input-group-prepend"\> <span class\="input-group-text"\>@</span\> </div\> <input type\="text" class\="form-control" placeholder\="Username"\> </div\> <div class\="input-group mb-3"\> <input type\="text" class\="form-control" placeholder\="Your Email"\> <div class\="input-group-append"\> <span class\="input-group-text"\>@runoob.com</span\> </div\> </div\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_input_group)

* * *

## 输入框大小

使用 .input-group-sm 类来设置小的输入框， .input-group-lg 类设置大的输入框：

## Bootstrap4 实例

<form\> <div class\="input-group mb-3 input-group-sm"\> <div class\="input-group-prepend"\> <span class\="input-group-text"\>Small</span\> </div\> <input type\="text" class\="form-control"\> </div\> </form\> <form\> <div class\="input-group mb-3"\> <div class\="input-group-prepend"\> <span class\="input-group-text"\>Default</span\> </div\> <input type\="text" class\="form-control"\> </div\> </form\> <form\> <div class\="input-group mb-3 input-group-lg"\> <div class\="input-group-prepend"\> <span class\="input-group-text"\>Large</span\> </div\> <input type\="text" class\="form-control"\> </div\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_input_group_size)

* * *

## 多个输入框和文本

## Bootstrap4 实例

<!-- 多个输入框 \--> <form\> <div class\="input-group mb-3"\> <div class\="input-group-prepend"\> <span class\="input-group-text"\>Person</span\> </div\> <input type\="text" class\="form-control" placeholder\="First Name"\> <input type\="text" class\="form-control" placeholder\="Last Name"\> </div\> </form\> <!-- 多个文本信息 \--> <form\> <div class\="input-group mb-3"\> <div class\="input-group-prepend"\> <span class\="input-group-text"\>One</span\> <span class\="input-group-text"\>Two</span\> <span class\="input-group-text"\>Three</span\> </div\> <input type\="text" class\="form-control"\> </div\> </form\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_input_group_multiple)

* * *

## 复选框与单选框

文本信息可以使用复选框与单选框替代：

![](https://www.runoob.com/wp-content/uploads/2018/06/214FC0E4-82F0-4597-826B-E1C7B0B5F356.jpg)

## Bootstrap4 实例

<div class\="input-group mb-3"\> <div class\="input-group-prepend"\> <div class\="input-group-text"\> <input type\="checkbox"\> </div\> </div\> <input type\="text" class\="form-control" placeholder\="RUNOOB"\> </div\> <div class\="input-group mb-3"\> <div class\="input-group-prepend"\> <div class\="input-group-text"\> <input type\="radio"\> </div\> </div\> <input type\="text" class\="form-control" placeholder\="GOOGLE"\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_input_group_check)

* * *

## 输入框添加按钮组

## Bootstrap4 实例

<div class\="input-group mb-3"\> <div class\="input-group-prepend"\> <button class\="btn btn-outline-secondary" type\="button"\>Basic Button</button\> </div\> <input type\="text" class\="form-control" placeholder\="Some text"\> </div\> <div class\="input-group mb-3"\> <input type\="text" class\="form-control" placeholder\="Search"\> <div class\="input-group-append"\> <button class\="btn btn-success" type\="submit"\>Go</button\> </div\> </div\> <div class\="input-group mb-3"\> <input type\="text" class\="form-control" placeholder\="Something clever.."\> <div class\="input-group-append"\> <button class\="btn btn-primary" type\="button"\>OK</button\> <button class\="btn btn-danger" type\="button"\>Cancel</button\> </div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_input_group_btn)

* * *

## 设置下拉菜单

输入框中添加下拉菜单不需要使用 .dropdown 类。

![](https://www.runoob.com/wp-content/uploads/2018/06/CE65025A-B840-45FA-BA3B-5173634CE5F2.jpg)

## Bootstrap4 实例

<div class\="input-group mt-3 mb-3"\> <div class\="input-group-prepend"\> <button type\="button" class\="btn btn-outline-secondary dropdown-toggle" data-toggle\="dropdown"\> 选择网站 </button\> <div class\="dropdown-menu"\> <a class\="dropdown-item" href\="https://www.google.com"\>GOOGLE</a\> <a class\="dropdown-item" href\="https://www.runoob.com"\>RUNOOB</a\> <a class\="dropdown-item" href\="https://www.taobao.com"\>TAOBAO</a\> </div\> </div\> <input type\="text" class\="form-control" placeholder\="网站地址"\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_input_group_dropdown)

* * *

## 输入框组标签

在输入框组通过在输入框组外围的 label 来设置标签，标签的 for 属性需要与输入框组的 id 对应，点击标签后可以聚焦输入框：

![](https://www.runoob.com/wp-content/uploads/2018/06/9F8A9143-892B-4A8A-901A-37C1E4E55941.jpg)

## Bootstrap4 实例

<label for\="demo"\>Write your email here:</label\> <div class\="input-group mb-3"\> <input type\="text" class\="form-control" placeholder\="Email" id\="demo" name\="email"\> <div class\="input-group-append"\> <span class\="input-group-text"\>@runoob.com</span\> </div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_form_input_group_labels)