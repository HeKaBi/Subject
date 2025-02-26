## Bootstrap4 提示框

提示框是一个小小的弹窗，在鼠标移动到元素上显示，鼠标移到元素外就消失。

* * *

## 如何创建提示框

通过向元素添加 data-toggle="tooltip" 来来创建提示框。

title 属性的内容为提示框显示的内容：

<a href\="#" data-toggle\="tooltip" title\="我是提示内容!"\>鼠标移动到我这</a\>

**注意:** 提示框要写在 jQuery 的初始化代码里: 然后在指定的元素上调用 tooltip() 方法。

以下实例可以在文档的任何地方使用提示框：

## 实例

$(document).ready(function(){ $('\[data-toggle="tooltip"\]').tooltip(); });

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_tooltip)

* * *

## 指定提示框的位置

默认情况下提示框显示在元素上方。

可以使用 data-placement 属性来设定提示框显示的方向: top, bottom, left 或 right:

## 实例

<a href\="#" data-toggle\="tooltip" data-placement\="top" title\="我是提示内容!"\>鼠标移动到我这</a\> <a href\="#" data-toggle\="tooltip" data-placement\="bottom" title\="我是提示内容!"\>鼠标移动到我这</a\> <a href\="#" data-toggle\="tooltip" data-placement\="left" title\="我是提示内容!"\>鼠标移动到我这</a\> <a href\="#" data-toggle\="tooltip" data-placement\="right" title\="我是提示内容!"\>鼠标移动到我这</a\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_tooltip_pos)

在按钮中使用:

## 实例

<button type\="button" class\="btn btn-secondary" data-toggle\="tooltip" data-placement\="top" title\="Tooltip on top"\> Tooltip on top </button\> <button type\="button" class\="btn btn-secondary" data-toggle\="tooltip" data-placement\="right" title\="Tooltip on right"\> Tooltip on right </button\> <button type\="button" class\="btn btn-secondary" data-toggle\="tooltip" data-placement\="bottom" title\="Tooltip on bottom"\> Tooltip on bottom </button\> <button type\="button" class\="btn btn-secondary" data-toggle\="tooltip" data-placement\="left" title\="Tooltip on left"\> Tooltip on left </button\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_tooltip_pos2)

提示内容添加 HTML 标签，设置 data-html="true"，内容放在 title 标签里头:

## 实例

<button type\="button" class\="btn btn-secondary" data-toggle\="tooltip" data-html\="true" title\="<em>Tooltip</em> <u>with</u> <b>HTML</b>"\> Tooltip with HTML </button\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_tooltip_pos3)

禁用按钮：

## 实例

<span class\="d-inline-block" tabindex\="0" data-toggle\="tooltip" title\="Disabled tooltip"\> <button class\="btn btn-primary" style\="pointer-events: none;" type\="button" disabled\>Disabled button</button\> </span\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_tooltip_pos4)