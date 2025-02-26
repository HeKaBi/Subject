## Tailwind CSS 基础概念

Tailwind CSS 是一个高度可定制的 CSS 框架，它提供了一套预定义的工具类，允许开发者快速构建和设计用户界面。

以下是 Tailwind CSS 的一些基础概念和用法：

| **概念**                   | **说明**                                                     |
| -------------------------- | ------------------------------------------------------------ |
| **工具类 (Utility-First)** | Tailwind CSS 的核心是工具类，用于快速设置样式，直接应用到 HTML 元素上。 |
| **响应式前缀**             | 使用如 `sm:`, `md:`, `lg:`, `xl:` 的前缀来控制不同屏幕尺寸下的样式。 |
| **颜色和尺寸**             | 提供了预定义的颜色（如 `bg-red-500`）和尺寸（如 `text-lg`）来快速设置样式。 |
| **间距 (Spacing)**         | 通过 `p-`, `m-`, `pt-`, `pr-` 等类控制内边距和外边距。       |
| **布局 (Layout)**          | 提供 `flex`, `grid`, `float` 等类来实现布局控制。            |
| **文本样式**               | 包括文本对齐、字体样式、颜色和转换的实用类，如 `text-center`, `font-bold`, `uppercase`。 |
| **背景和边框**             | 提供背景颜色、背景图片、边框样式和颜色的工具类，如 `bg-gray-200`, `border-red-500`。 |
| **悬停和状态**             | 使用 `hover:`, `focus:`, `active:` 等前缀为交互状态定义样式。 |
| **尺寸 (Sizing)**          | 使用 `w-`, `h-` 类控制宽度和高度，如 `w-64`, `h-screen`。    |
| **可见性 (Visibility)**    | 使用 `visible`, `invisible` 等类控制元素的可见性。           |
| **栅格系统 (Grid System)** | 提供基于 CSS Grid 的工具类，如 `grid`, `grid-cols-3`, `col-span-2`，实现响应式网格布局。 |
| **自定义配置**             | 通过 `tailwind.config.js` 自定义颜色、间距、字体大小等，以适应项目需求。 |
| **暗色模式 (Dark Mode)**   | 支持暗色模式，通过 `dark:` 前缀设置样式，并可在配置中启用暗色模式功能。 |
| **插件 (Plugins)**         | 通过插件扩展功能，添加自定义的工具类或功能。                 |
| **指令 (Directives)**      | 在 CSS 文件中使用 `@tailwind` 指令引入不同层次的样式，如 `base`, `components`, `utilities`。 |

## 概念详解

### 1\. **工具类（Utility-First）**

Tailwind 的工具类可以让开发者快速定义样式，无需手动编写 CSS。

## 实例

<div class\="text-center text-blue-500 font-bold"\>  
  Tailwind Utility Classes  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic1)

解析：

+   `text-center`：居中对齐。
+   `text-blue-500`：蓝色文字。
+   `font-bold`：加粗字体。

* * *

### 2\. **响应式前缀**

通过前缀设置不同屏幕尺寸下的样式。

## 实例

<div class\="bg-red-500 sm:bg-green-500 md:bg-blue-500 lg:bg-yellow-500"\>  
  Responsive Example  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic2)

解析：

+   默认：红色背景。
+   小屏幕（≥640px）：绿色背景。
+   中屏幕（≥768px）：蓝色背景。
+   大屏幕（≥1024px）：黄色背景。

* * *

### 3\. **颜色和尺寸**

Tailwind 提供了丰富的预定义颜色和尺寸，便于快速应用。

## 实例

<p class\="text-lg text-gray-600"\>  
  Text with pre-defined size and color  
</p\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic3)

解析：

+   `text-lg`：文字大小。
+   `text-gray-600`：灰色文字。

* * *

### 4\. **间距（Spacing）**

通过间距工具类设置元素的内外边距。

## 实例

<div class\="p-4 m-8"\>  
  Padding and Margin Example  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic4)

解析：

+   `p-4`：内边距为 1rem。
+   `m-8`：外边距为 2rem。

* * *

### 5\. **布局（Layout）**

提供的类可以快速实现灵活的布局方式，如 Flexbox 和 Grid。

## 实例

<div class\="flex justify-between items-center"\>  
  <div\>Item 1</div\>  
  <div\>Item 2</div\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic5-1)

**Grid 实例：**

## 实例

<div class\="grid grid-cols-3 gap-4"\>  
  <div\>1</div\>  
  <div\>2</div\>  
  <div\>3</div\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic5-2)

* * *

### 6\. **文本样式**

控制文本的对齐、颜色、大小和其他样式。

## 实例

<p class\="text-center font-semibold text-red-500"\>  
  Centered Bold Text  
</p\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic6)

* * *

### 7\. **背景和边框**

通过工具类设置背景颜色、图片和边框样式。

## 实例

<div class\="bg-yellow-200 border border-gray-400"\>  
  Background and Border Example  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic7)

* * *

### 8\. **悬停和状态**

为交互元素设置状态样式。

## 实例

<button class\="bg-blue-500 hover:bg-blue-700 text-white"\>  
  Hover Me  
</button\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic8)

* * *

### 9\. **尺寸（Sizing）**

设置元素的宽度和高度。

## 实例

<div class\="w-64 h-32 bg-gray-300"\>  
  Width and Height  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic9)

* * *

### 10\. **可见性（Visibility）**

控制元素的显示与隐藏。

## 实例

<div class\="invisible sm:visible"\>  
  Visible only on small screens  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic10)

* * *

### 11\. **栅格系统（Grid System）**

使用 Tailwind 的 Grid 工具类创建网格布局。

## 实例

<div class\="grid grid-cols-3 gap-2"\>  
  <div\>1</div\>  
  <div\>2</div\>  
  <div\>3</div\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic11)

* * *

### 12\. **自定义配置**

通过配置文件自定义设计系统。

## 实例

// tailwind.config.js  
module.exports \= {  
  theme: {  
    extend: {  
      colors: {  
        primary: '#1D4ED8',  
      },  
    },  
  },  
}  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic12)

* * *

### 13\. **暗色模式**

启用暗模式并定义样式。

## 实例

<div class\="bg-white dark:bg-black text-black dark:text-white"\>  
  Dark Mode Example  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_basic13)

* * *

### 14\. **插件**

通过插件扩展 Tailwind 的功能。

## 实例

// tailwind.config.js  
const plugin \= require('tailwindcss/plugin')  
module.exports \= {  
  plugins: \[  
    plugin(function({ addUtilities }) {  
      addUtilities({  
        '.rotate-45': {  
          transform: 'rotate(45deg)',  
        },  
      })  
    }),  
  \],  
}  

* * *

### 15\. **指令（Directives）**

通过 `@tailwind` 指令加载 Tailwind 的不同层。

## 实例

@tailwind base;  
@tailwind components;  
@tailwind utilities;