## Bootstrap4 导航

如果你想创建一个简单的水平导航栏，可以在 <ul> 元素上添加 .nav类，在每个 <li> 选项上添加 .nav-item 类，在每个链接上添加 .nav-link 类:

## 实例

<ul class\="nav"\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link disabled" href\="#"\>Disabled</a\> </li\> </ul\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav)

* * *

## 导航对齐方式

.justify-content-center 类设置导航居中显示， .justify-content-end 类设置导航右对齐。

## 实例

<!-- 导航居中 \--> <ul class\="nav justify-content-center"\> <!-- 导航右对齐 \--> <ul class\="nav justify-content-end"\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_align)

* * *

## 垂直导航

.flex-column 类用于创建垂直导航：

## 实例

<ul class\="nav flex-column"\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_vertical)

* * *

## 选项卡

使用 .nav-tabs 类可以将导航转化为选项卡。然后对于选中的选项使用 .active 类来标记。

## 实例

<ul class\="nav nav-tabs"\> <li class\="nav-item"\> <a class\="nav-link active" href\="#"\>Active</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link disabled" href\="#"\>Disabled</a\> </li\> </ul\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_tabs)

* * *

## 胶囊导航

.nav-pills 类可以将导航项设置成胶囊形状。

## 实例

<ul class\="nav nav-pills"\> <li class\="nav-item"\> <a class\="nav-link active" href\="#"\>Active</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link disabled" href\="#"\>Disabled</a\> </li\> </ul\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_pills)

* * *

## 导航等宽

.nav-justified 类可以设置导航项齐行等宽显示。

## 实例

<ul class\="nav nav-pills nav-justified"\>..</ul\> <ul class\="nav nav-tabs nav-justified"\>..</ul\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_justified)

* * *

## 胶囊下拉菜单

## 实例

<ul class\="nav nav-pills"\> <li class\="nav-item"\> <a class\="nav-link active" href\="#"\>Active</a\> </li\> <li class\="nav-item dropdown"\> <a class\="nav-link dropdown-toggle" data-toggle\="dropdown" href\="#"\>Dropdown</a\> <div class\="dropdown-menu"\> <a class\="dropdown-item" href\="#"\>Link 1</a\> <a class\="dropdown-item" href\="#"\>Link 2</a\> <a class\="dropdown-item" href\="#"\>Link 3</a\> </div\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link disabled" href\="#"\>Disabled</a\> </li\> </ul\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_pills_dropdown)

* * *

## 选项卡下拉菜单

## 实例

<ul class\="nav nav-tabs"\> <li class\="nav-item"\> <a class\="nav-link active" href\="#"\>Active</a\> </li\> <li class\="nav-item dropdown"\> <a class\="nav-link dropdown-toggle" data-toggle\="dropdown" href\="#"\>Dropdown</a\> <div class\="dropdown-menu"\> <a class\="dropdown-item" href\="#"\>Link 1</a\> <a class\="dropdown-item" href\="#"\>Link 2</a\> <a class\="dropdown-item" href\="#"\>Link 3</a\> </div\> </li\> <li class\="nav-item"\> <a class\="nav-link" href\="#"\>Link</a\> </li\> <li class\="nav-item"\> <a class\="nav-link disabled" href\="#"\>Disabled</a\> </li\> </ul\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_tabs_dropdown)

* * *

## 动态选项卡

如果你要设置选项卡是动态可切换的，可以在每个链接上添加 data-toggle="tab" 属性。 然后在每个选项对应的内容的上添加 .tab-pane 类，对应选项卡内容的 <div> 元素使用 .tab-content 类 。。

如果你希望有淡入效果可以在 .tab-pane 后添加 .fade类:

## 实例

<!-- Nav tabs \--> <ul class\="nav nav-tabs"\> <li class\="nav-item"\> <a class\="nav-link active" data-toggle\="tab" href\="#home"\>Home</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" data-toggle\="tab" href\="#menu1"\>Menu 1</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" data-toggle\="tab" href\="#menu2"\>Menu 2</a\> </li\> </ul\> <!-- Tab panes \--> <div class\="tab-content"\> <div class\="tab-pane active container" id\="home"\>...</div\> <div class\="tab-pane container" id\="menu1"\>...</div\> <div class\="tab-pane container" id\="menu2"\>...</div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_tabs_toggleable)

* * *

## 胶囊状动态选项卡

胶囊状动态选项卡只需要将以上实例的代码中 data-toggle 属性设置为 data-toggle="pill":

## 实例

<!-- Nav pills \--> <ul class\="nav nav-pills"\> <li class\="nav-item"\> <a class\="nav-link active" data-toggle\="pill" href\="#home"\>Home</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" data-toggle\="pill" href\="#menu1"\>Menu 1</a\> </li\> <li class\="nav-item"\> <a class\="nav-link" data-toggle\="pill" href\="#menu2"\>Menu 2</a\> </li\> </ul\> <!-- Tab panes \--> <div class\="tab-content"\> <div class\="tab-pane active container" id\="home"\>...</div\> <div class\="tab-pane container" id\="menu1"\>...</div\> <div class\="tab-pane container" id\="menu2"\>...</div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_nav_pills_toggleable)