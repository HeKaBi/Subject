## Tailwind CSS 安装(CDN)

如果只想简单体验，可以直接引入 CDN 链接：

使用官网提供的 CDN 库，地址如下：

<script src\="https://cdn.tailwindcss.com"\></script\>  

使用 jsDelivr 的 CDN 库，地址如下：

<link href\="https://cdn.jsdelivr.net/npm/tailwindcss@3.3.0/dist/tailwind.min.css" rel\="stylesheet"\>

使用这种方式使用：

+   **优点：**无需配置，适合快速开发和演示。
+   **缺点：**不能自定义样式，文件体积较大。

### 使用实例

以下实例输出了 Hello, world!

## 实例

<!doctype html\> <html\> <head\> <meta charset\="UTF-8"\> <meta name\="viewport" content\="width=device-width, initial-scale=1.0"\> <script src\="https://cdn.tailwindcss.com"\></script\> </head\> <body\> <h1 class\="text-3xl font-bold underline"\> Hello world! </h1\> </body\> </html\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_hw)

编辑 tailwind.config 对象可以定义自己的配置信息：

## 实例

<!doctype html\> <html\> <head\> <meta charset\="UTF-8"\> <meta name\="viewport" content\="width=device-width, initial-scale=1.0"\> <script src\="https://cdn.tailwindcss.com"\></script\> <script\> tailwind.config = { theme: { extend: { colors: { clifford: '#da373d', } } } } </script\> </head\> <body\> <h1 class\="text-3xl font-bold underline text-clifford"\> Hello world! </h1\> </body\> </html\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_hw2)

使用 type="text/tailwindcss" 添加自定义 CSS：

## 实例

<!doctype html>  
<html\>  
<head\>  
  <meta charset\="UTF-8"\>  
  <meta name\="viewport" content\="width=device-width, initial-scale=1.0"\>  
  <script src\="https://cdn.tailwindcss.com"\></script\>  
  <style type\="text/tailwindcss"\>  
    @layer utilities {  
      .content-auto {  
        content-visibility: auto;  
      }  
    }  
  </style\>  
</head\>  
<body\>  
  <div class\="lg:content-auto"\>  
    <!-- ... -->  
  </div\>  
</body\>  
</html\>  

使用 plugins 参数可以设置使用的插件，如 forms（表单） 和 typography（排版）：

## 实例

<!doctype html>  
<html\>  
<head\>  
  <meta charset\="UTF-8"\>  
  <meta name\="viewport" content\="width=device-width, initial-scale=1.0"\>  
  <script src\="https://cdn.tailwindcss.com?plugins=forms,typography,aspect-ratio,line-clamp,container-queries"\></script\>  
</head\>  
<body\>  
  <div class\="prose"\>  
    <!-- ... -->  
  </div\>  
</body\>  
</html\>