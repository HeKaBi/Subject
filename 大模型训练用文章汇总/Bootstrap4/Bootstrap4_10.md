## Bootstrap4 按钮

Bootstrap 4 提供了不同样式的按钮。

## 实例

```html
<button type\="button" class\="btn"\>基本按钮</button\>
<button type\="button" class\="btn btn-primary"\>主要按钮</button\>
<button type\="button" class\="btn btn-secondary"\>次要按钮</button\> <button type\="button" class\="btn btn-success"\>成功</button\>
<button type\="button" class\="btn btn-info"\>信息</button\> <button type\="button" class\="btn btn-warning"\>警告</button\>
<button type\="button" class\="btn btn-danger"\>危险</button\> <button type\="button" class\="btn btn-dark"\>黑色</button\>
<button type\="button" class\="btn btn-light"\>浅色</button\> <button type\="button" class\="btn btn-link"\>链接</button\>
```



[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_button_styles)

按钮类可用于 <a>, <button>, 或 <input> 元素上:

## 实例

```html
<a href\="#" class\="btn btn-info" role\="button"\>链接按钮</a\> 
<button type\="button" class\="btn btn-info"\>按钮</button\> 
<input type\="button" class\="btn btn-info" value\="输入框按钮"\> 
<input type\="submit" class\="btn btn-info" value\="提交按钮"\>
```



[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_button_elements)

* * *

## 按钮设置边框

## 实例

```html
<button type\="button" class\="btn btn-outline-primary"\>主要按钮</button\>
<button type\="button" class\="btn btn-outline-secondary"\>次要按钮</button\>
<button type\="button" class\="btn btn-outline-success"\>成功</button\>
<button type\="button" class\="btn btn-outline-info"\>信息</button\> <button type\="button" class\="btn btn-outline-warning"\>警告</button\>
<button type\="button" class\="btn btn-outline-danger"\>危险</button\> <button type\="button" class\="btn btn-outline-dark"\>黑色</button\>
<button type\="button" class\="btn btn-outline-light text-dark"\>浅色</button\>
```



[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_button_outline)

* * *

## 不同大小的按钮

Bootstrap 4 可以设置按钮的大小：

## 实例

```html
<button type\="button" class\="btn btn-primary btn-lg"\>大号按钮</button\> 
<button type\="button" class\="btn btn-primary"\>默认按钮</button\> 
<button type\="button" class\="btn btn-primary btn-sm"\>小号按钮</button\>
```



[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_button_sizes)

* * *

## 块级按钮

通过添加 .btn-block 类可以设置块级按钮：

## 实例

```html
<button type\="button" class\="btn btn-primary btn-block"\>按钮 1</button\>
```



[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_button_block)

* * *

## 激活和禁用的按钮

按钮可设置为激活或者禁止点击的状态。

.active 类可以设置按钮是可用的， disabled 属性可以设置按钮是不可点击的。 注意 <a> 元素不支持 disabled 属性，你可以通过添加 .disabled 类来禁止链接的点击。

## 实例

```html
<button type\="button" class\="btn btn-primary active"\>点击后的按钮</button\>
<button type\="button" class\="btn btn-primary" disabled\>禁止点击的按钮</button\>
<a href\="#" class\="btn btn-primary disabled"\>禁止点击的链接</a\>
```



[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_button_active)

* * *

## 加载按钮

我们也可以设置一个正在加载的按钮。

## 实例

```html
<button class\="btn btn-primary"\>
    <span class\="spinner-border spinner-border-sm"\></span\>
</button\>
<button class\="btn btn-primary"\>
    <span class\="spinner-border spinner-border-sm"\></span\> Loading.. 
</button\>
<button class\="btn btn-primary" disabled\> 
    <span class\="spinner-border spinner-border-sm"\></span\> Loading.. 
</button\> 
<button class\="btn btn-primary" disabled\> 
    <span class\="spinner-grow spinner-grow-sm"\></span\> Loading.. 
</button\>
```



[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_spinners_buttons)