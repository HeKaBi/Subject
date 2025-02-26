## Bootstrap4 徽章（Badges）

![](https://www.runoob.com/wp-content/uploads/2017/10/00AF5E64-DA63-43FF-81DA-CA9A774E4F67.jpg)

徽章（Badges）主要用于突出显示新的或未读的项。如需使用徽章，只需要将 .badge 类加上带有指定意义的颜色类 (如 .badge-secondary) 添加到 <span> 元素上即可。 徽章可以根据父元素的大小的变化而变化:

## 实例

```html
<h1\>测试标题 <span class\="badge badge-secondary"\>New</span\></h1\> 
<h2\>测试标题 <span class\="badge badge-secondary"\>New</span\></h2\> 
<h3\>测试标题 <span class\="badge badge-secondary"\>New</span\></h3\> 
<h4\>测试标题 <span class\="badge badge-secondary"\>New</span\></h4\> 
<h5\>测试标题 <span class\="badge badge-secondary"\>New</span\></h5\> 
<h6\>测试标题 <span class\="badge badge-secondary"\>New</span\></h6\>
```

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_badges)

* * *

## 各种颜色类型的徽章

以下列出了所有颜色类型的徽章:

## 实例

```html
<span class\="badge badge-primary"\>主要</span\> 
<span class\="badge badge-secondary"\>次要</span\> 
<span class\="badge badge-success"\>成功</span\> 
<span class\="badge badge-danger"\>危险</span\> 
<span class\="badge badge-warning"\>警告</span\> 
<span class\="badge badge-info"\>信息</span\> 
<span class\="badge badge-light"\>浅色</span\> 
<span class\="badge badge-dark"\>深色</span\>
```

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_badges2)

* * *

## 药丸形状徽章

使用 .badge-pill 类来设置药丸形状徽章:

## 实例

```html
<span class\="badge badge-pill badge-default"\>默认</span\> 
<span class\="badge badge-pill badge-primary"\>主要</span\> 
<span class\="badge badge-pill badge-success"\>成功</span\> 
<span class\="badge badge-pill badge-info"\>信息</span\> 
<span class\="badge badge-pill badge-warning"\>警告</span\> 
<span class\="badge badge-pill badge-danger"\>危险</span\>
```

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_badges_pills)

* * *

## 徽章插入到元素内

以下实例将徽章嵌入到按钮内：

## 实例

```html
<button type\="button" class\="btn btn-primary"\> Messages <span class\="badge badge-light"\>4</span\> </button\>
```

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_badges_button)