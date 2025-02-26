## Bootstrap4 多媒体对象

Bootstrap 提供了很好的方式来处理多媒体对象（图片或视频）和内容的布局。应用场景有博客评论、微博等:

## 基础多媒体对象

要创建一个多媒体对象，可以在容器元素上添加 .media 类，然后将多媒体内容放到子容器上，子容器需要添加 .media-body 类，然后添加外边距，内边距等效果:

## 实例

<div class\="media border p-3"\> <img src\="mobile-icon.png" alt\="John Doe" class\="mr-3 mt-3 rounded-circle" style\="width:60px;"\> <div class\="media-body"\> <h4\>菜鸟教程</h4\> <p\>学的不仅是技术，更是梦想！！！</p\> </div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_media)

* * *

## 多媒体对象嵌套

多媒体对象可以多个嵌套（一个多媒体对象中包含另外一个多媒体对象）

要嵌套多媒体对象，可以把新的 .media 容器放到 .media-body 容器中:

## 实例

<div class\="media border p-3"\> <img src\="mobile-icon.png" alt\="John Doe" class\="mr-3 mt-3 rounded-circle" style\="width:60px;"\> <div class\="media-body"\> <h4\>菜鸟教程</h4\> <p\>学的不仅是技术，更是梦想！！！</p\> <div class\="media p-3"\> <img src\="mobile-icon.png" alt\="Jane Doe" class\="mr-3 mt-3 rounded-circle" style\="width:45px;"\> <div class\="media-body"\> <h4\>菜鸟教程</h4\> <p\>学的不仅是技术，更是梦想！！！</p\> </div\> </div\> </div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_media_nested)

* * *

## 多媒体对象图片显示在右边

如果你想将头像图片显示在右侧，可以在 .media-body 容器后添加图片:

## 实例

<div class\="media border p-3"\> <div class\="media-body"\> <h4\>菜鸟教程</h4\> <p\>学的不仅是技术，更是梦想！！！</p\> </div\> <img src\="mobile-icon.png" alt\="John Doe" class\="ml-3 mt-3 rounded-circle" style\="width:60px;"\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_media_right)

* * *

## 定位多媒体图片位置

我们可以使用 align-self-\* 相关类来设置多媒体对象的图片显示位置：

## 实例

<!-- 头部 \--> <div class\="media"\> <img src\="https://static.jyshare.com/images/mobile-icon.png" class\="align-self-start mr-3" style\="width:60px"\> <div class\="media-body"\> <h4\>头部 -- 菜鸟教程</h4\> <p\>学的不仅是技术，更是梦想！！！</p\> </div\> </div\> <!-- 居中 \--> <div class\="media"\> <img src\="https://static.jyshare.com/images/mobile-icon.png" class\="align-self-center mr-3" style\="width:60px"\> <div class\="media-body"\> <h4\>居中 -- 菜鸟教程</h4\> <p\>学的不仅是技术，更是梦想！！！</p\> </div\> </div\> <!-- 底部 \--> <div class\="media"\> <img src\="https://static.jyshare.com/images/mobile-icon.png" class\="align-self-end mr-3" style\="width:60px"\> <div class\="media-body"\> <h4\>底部 -- 菜鸟教程</h4\> <p\>学的不仅是技术，更是梦想！！！</p\> </div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_media_alignment)