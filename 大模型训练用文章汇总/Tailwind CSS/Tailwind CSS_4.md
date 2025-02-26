## Tailwind CSS 安装(NPM)

在开始之前，确保你已经安装了 Node.js 和 npm，你可以通过以下命令检查它们是否已经安装：

```
node -v
npm -v
```

如果你的系统还不支持 Node.js 及 NPM 可以参考我们的 [Node.js 教程](httsp://www.runoob.com/nodejs/nodejs-tutorial.html)。

国内使用 npm 速度很慢，你可以使用淘宝定制的 cnpm (gzip 压缩支持) 命令行工具代替默认的 npm:

```
$ npm install -g cnpm --registry=https://registry.npmmirror.com
$ npm config set registry https://registry.npmmirror.com
```

这样就可以使用 cnpm 命令来安装模块了：

```
$ cnpm install [name]
```

更多信息可以查阅：[http://npm.taobao.org/](http://npm.taobao.org/)。

* * *

## 安装 Tailwind CSS

通过 npm 安装 在本地项目中安装并配置 Tailwind CSS：

```
npm install -D tailwindcss
npx tailwindcss init
```

执行以上命令后，会生成一个基础配置文件 tailwind.config.js，供定制使用。

### 配置模板路径

接下来我们可以在 tailwind.config.js 文件中添加模版的路径：

## tailwind.config.js 文件代码：

/\*\* @type {import('tailwindcss').Config} \*/  
module.exports \= {  
  content: \["./src/\*\*/\*.{html,js}"\],  // 根据项目实际文件类型调整  
  theme: {  
    extend: {},  
  },  
  plugins: \[\],  
}  

### 添加 Tailwind 指令到 CSS 文件

在你的主 CSS 文件 src/input.css（没有就创建它） 中通过 @tailwind 指令添加每一 个Tailwind 功能模块。

## src/input.css 文件代码：

@tailwind base;  
@tailwind components;  
@tailwind utilities;  

### 启动 Tailwind CLI 构建流程

运行CLI工具以扫描模板文件中的类并构建CSS。

```
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

### 在 HTML 中使用 Tailwind

将编译好的 CSS 文件添加到 <head> 标签内，然后就可以开始使用 Tailwind 的工具类来为你的内容设置样式了。

## src/index.html 文件代码：

<!doctype html>  
<html\>  
<head\>  
  <meta charset\="UTF-8"\>  
  <meta name\="viewport" content\="width=device-width, initial-scale=1.0"\>  
  <link href\="./output.css" rel\="stylesheet"\>  
</head\>  
<body\>  
  <h1 class\="text-3xl font-bold underline"\>  
    Hello world!  
  </h1\>  
</body\>  
</html\>  

以上步骤适用于大多数现代前端项目，无论是使用 Vue、React 还是其他框架，确保在构建过程中引入了编译后的 CSS 文件，以便 Tailwind CSS 的样式能够正确应用到你的项目中。

* * *

## 使用 PostCSS

将 Tailwind CSS 作为 PostCSS 插件安装，是与构建工具（如 webpack、Rollup、Vite 和 Parcel）无缝集成的最佳方式。

### 1、安装 Tailwind CSS

通过 npm 安装 Tailwind CSS 及其相关依赖，并生成 tailwind.config.js 配置文件。

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
```

### 2、将 Tailwind 添加到 PostCSS 配置

在项目的 postcss.config.js 文件中，添加 tailwindcss 和 autoprefixer 插件。

## postcss.config.js 文件代码：

module.exports \= {  
  plugins: {  
    tailwindcss: {},  
    autoprefixer: {},  
  }  
}  

### 3、配置模板路径

在 tailwind.config.js 文件中，添加所有模板文件的路径，以便 Tailwind CSS 能够根据这些文件生成所需的样式。

## tailwind.config.js 文件代码：

/\*\* @type {import('tailwindcss').Config} \*/  
module.exports \= {  
  content: \["./src/\*\*/\*.{html,js}"\], // 替换为项目中实际的模板路径  
  theme: {  
    extend: {},  
  },  
  plugins: \[\],  
}  

### 4、在 CSS 文件中添加 Tailwind 指令

在主 CSS 文件中，添加以下三个 Tailwind 的核心指令，用于引入基础样式、组件样式和工具类样式。

## main.css 文件代码：

@tailwind base;  
@tailwind components;  
@tailwind utilities;  

### 5、启动构建过程

通过 npm run dev 或 package.json 文件中配置的相关命令，启动项目的构建过程。

```
npm run dev
```

### 6、在 HTML 中使用 Tailwind CSS

确保编译后的 CSS 文件被正确引入到 <head> 标签中（某些框架可能会自动完成这一步），然后开始在 HTML 中使用 Tailwind CSS 提供的实用类来为内容添加样式。

## index.html 文件代码：

<!doctype html>  
<html\>  
<head\>  
  <meta charset\="UTF-8"\>  
  <meta name\="viewport" content\="width=device-width, initial-scale=1.0"\>  
  <link href\="/dist/main.css" rel\="stylesheet"\> <!-- 引入编译后的 CSS 文件 -->  
</head\>  
<body\>  
  <h1 class\="text-3xl font-bold underline"\>  
    Hello world!  
  </h1\>  
</body\>  
</html\>