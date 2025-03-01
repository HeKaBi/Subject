## JSON \- 简介

* * *

## 在线实例

通过我们的编辑器，您可以在线编辑 JavaScript 代码，然后通过点击一个按钮来查看结果：

## JSON 实例

<!DOCTYPE html\> <html\> <head\> <meta charset\="utf-8"\> <title\>菜鸟教程(runoob.com)</title\> </head\> <body\> <h2\>JavaScript 创建 JSON 对象</h2\> <p\> 网站名称: <span id\="jname"\></span\><br /> 网站地址: <span id\="jurl"\></span\><br /> 网站 slogan: <span id\="jslogan"\></span\><br /> </p\> <script\>

var JSONObject\= { "name":"菜鸟教程", "url":"www.runoob.com", "slogan":"学的不仅是技术，更是梦想！" }; document.getElementById("jname").innerHTML\=JSONObject.name document.getElementById("jurl").innerHTML\=JSONObject.url document.getElementById("jslogan").innerHTML\=JSONObject.slogan

</script\> </body\> </html\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=tryjson_create)  
点击 "尝试一下" 按钮查看在线实例。

  

* * *

## 与 XML 相同之处

+   JSON 是纯文本
+   JSON 具有"自我描述性"（人类可读）
+   JSON 具有层级结构（值中存在值）
+   JSON 可通过 JavaScript 进行解析
+   JSON 数据可使用 AJAX 进行传输

* * *

## 与 XML 不同之处

+   没有结束标签
+   更短
+   读写的速度更快
+   能够使用内建的 JavaScript eval() 方法进行解析
+   使用数组
+   不使用保留字

* * *

## 为什么使用 JSON？

对于 AJAX 应用程序来说，JSON 比 XML 更快更易使用：

#### 使用 XML

+   读取 XML 文档
+   使用 XML DOM 来循环遍历文档
+   读取值并存储在变量中

#### 使用 JSON

+   读取 JSON 字符串
+   用 eval() 处理 JSON 字符串