## Tailwind CSS 深色模式

深色模式（Dark Mode）是一种常见的用户界面设计趋势，提供暗色调的界面以减少眼睛疲劳，同时节省设备电量。

Tailwind CSS 支持深色模式（Dark Mode）的功能，使得开发者可以轻松地为网站创建深色版本，以适应用户的系统偏好。

Tailwind CSS 提供了一个名为 dark 的修饰符，允许你针对深色模式定义样式。

当用户设备或操作系统设置为深色模式时，带有 dark: 修饰符的样式将自动生效。

以下实例基于系统首选项的媒体查询设置样式：

## 实例

<div class\="bg-white text-black dark:bg-black dark:text-white"\>  
  该文本根据颜色模式而变化。  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_darkmode1)

**在浅色模式下：**背景色为白色（`bg-white`），文本颜色为黑色（`text-black`）。

**在深色模式下：**背景色为黑色（`dark:bg-black`），文本颜色为白色（`dark:text-white`）。

* * *

## 启用深色模式

默认情况下，Tailwind 使用 media 策略来检测深色模式，即基于用户的系统首选项。

如果需要更细粒度的控制，也可以使用 class 策略。

### 1、在 tailwind.config.js 中启用深色模式

## 实例

module.exports \= {  
  darkMode: 'media', // 基于系统首选项 (默认)  
  // darkMode: 'class', // 基于类名手动切换  
  theme: {  
    extend: {},  
  },  
  plugins: \[\],  
}  

+   **`media` 模式**：根据用户操作系统的设置（通过媒体查询 `prefers-color-scheme: dark`）自动切换。
+   **`class` 模式**：允许开发者通过在 `html` 或 `body` 标签上添加 `dark` 类手动切换深色模式。

**两种模式的差异:**

| 模式         | 检测方式                                     | 控制方式               | 使用场景                     |
| ------------ | -------------------------------------------- | ---------------------- | ---------------------------- |
| `media` 模式 | 基于系统首选项的媒体查询                     | 自动切换               | 简单应用场景，无需自定义逻辑 |
| `class` 模式 | 基于手动在 `html` 或 `body` 上添加 `dark` 类 | 由开发者自定义切换逻辑 | 需要按钮或切换器的复杂场景   |

### 切换逻辑示例（class 模式）

如果要支持手动切换深色模式而不是依赖于操作系统首选项，请使用 class 策略代替 media 策略。

现在，dark:{class} 类将不再根据 prefers-color-scheme 起作用，而是当在 HTML 树中出现 dark 类时起作用：

```
<!-- 不允许深色模式 -->
<html>
<body>
  <div class="bg-white dark:bg-black">...</div>
</body>
</html>

<!-- 允许深色模式 -->
<html class="dark">
<body>
  <div class="bg-white dark:bg-black">...</div>
</body>
</html>
```

## 实例

<button id\="toggle-dark-mode"\>Toggle Dark Mode</button\>  
<script\>  
const toggle = document.getElementById('toggle-dark-mode');  
toggle.addEventListener('click', () => {  
    document.documentElement.classList.toggle('dark');  
});  
</script\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_darkmode2)

* * *

## 如何使用深色模式工具类

### 1、样式切换

使用 dark: 前缀指定深色模式下的样式。

## 实例

<div class\="bg-gray-200 dark:bg-gray-800 text-gray-900 dark:text-gray-100"\>  
  可适应明暗模式的设计。  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_darkmode3)

### 2、响应式与深色模式结合

响应式断点和深色模式可以同时使用：

## 实例

<div class\="text-lg sm:text-xl dark:text-gray-300 sm:dark:text-gray-500"\>  
  响应式且支持深色模式的文本。  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_darkmode4)

小屏幕下字体为 xl。

在深色模式中，小屏幕的字体颜色变为浅灰色。

### 3、交互状态与深色模式结合

你可以结合 hover, focus 等状态与深色模式应用样式：

## 实例

<button class\="bg-white dark:bg-black text-black dark:text-white hover:bg-gray-300 dark:hover:bg-gray-700"\>  
  互动按钮  
</button\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_darkmode5)

## 扩展深色模式

在某些情况下，你可能需要针对深色模式提供额外的颜色或样式，可以通过 theme.extend 自定义 Tailwind 配置。

```
module.exports = {
  theme: {
    extend: {
      colors: {
        brand: {
          DEFAULT: '#1DA1F2',
          dark: '#0d74b8',
        },
      },
    },
  },
}
```

在 HTML 中使用扩展颜色：

## 实例

<div class\="text-brand dark:text-brand-dark"\>  
  定制深色模式颜色！  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_darkmode6)

* * *

## 实例

以下是一个实现深色模式切换的完整示例：

## 实例

<div class\="p-6"\>  
<h1\>欢迎来到深色模式</h1\>  
<button id\="toggle-dark-mode" class\="mt-4 bg-gray-200 dark:bg-gray-700 text-black dark:text-white p-2 rounded"\>  
    切换模式  
</button\>  
</div\>  
<script\>  
const toggle = document.getElementById('toggle-dark-mode');  
toggle.addEventListener('click', () => {  
    const isDark = document.documentElement.classList.toggle('dark');  
    localStorage.theme = isDark ? 'dark' : 'light';  
});  
</script\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_darkmode7)