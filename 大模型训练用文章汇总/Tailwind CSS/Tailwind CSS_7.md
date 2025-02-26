## Tailwind CSS 工具类（Utility-First）

Tailwind CSS 的工具类（Utility-First）是一种以实用为先的设计方法，它允许开发者直接在 HTML 元素上应用预定义的样式类，而无需编写传统的 CSS 代码。

Tailwind CSS 的核心理念是 工具类优先（Utility-First），这一设计思想意味着，你可以通过组合单一功能的 CSS 类来实现一个完整的样式，而不是依赖于复杂的自定义样式。

Tailwind CSS 提供了大量的工具类，每个类都执行一个简单的样式任务，例如，text-center 用来将文本居中，bg-blue-500 用来设置背景颜色，p-4 用来设置内边距等。

**常见的工具类：**

| **类别**                 | **工具类示例**                        | **描述**                                                    |
| ------------------------ | ------------------------------------- | ----------------------------------------------------------- |
| **排版（Typography）**   | `text-center`, `text-lg`, `font-bold` | 控制文本的对齐、字体大小、粗细等。                          |
| **背景（Background）**   | `bg-blue-500`, `bg-opacity-50`        | 设置元素的背景颜色、背景图和透明度。                        |
| **间距（Spacing）**      | `p-4`, `m-2`, `mt-8`                  | 控制元素的内外边距（padding 和 margin）。                   |
| **布局（Layout）**       | `flex`, `grid`, `block`               | 设置元素的显示类型和布局方式。                              |
| **尺寸（Sizing）**       | `w-32`, `h-48`                        | 设置元素的宽度和高度。                                      |
| **边框（Borders）**      | `border`, `border-2`, `rounded`       | 设置元素的边框、边框宽度和圆角。                            |
| **阴影（Shadows）**      | `shadow`, `shadow-lg`                 | 控制元素的阴影效果。                                        |
| **透明度（Opacity）**    | `opacity-50`, `opacity-100`           | 设置元素的透明度。                                          |
| **响应式（Responsive）** | `sm:text-lg`, `md:bg-blue-300`        | 控制不同屏幕尺寸下的样式变化。                              |
| **状态（State）**        | `hover:bg-blue-700`, `focus:ring-4`   | 设置元素在不同交互状态（如 hover、focus、active）下的样式。 |

### 工具类的优势

+   **简洁和高效**：每个工具类只负责一个小的样式操作，开发者可以根据需要组合不同的类，快速完成页面布局和样式。
+   **灵活性**：通过类的组合，几乎可以实现任何样式，无需编写复杂的 CSS 代码。
+   **响应式支持**：Tailwind 提供了内建的响应式类，可以非常方便地根据屏幕尺寸调整布局和样式。
+   **避免命名冲突**：由于每个类的作用非常明确且独立，使用工具类的方式避免了传统 CSS 中命名冲突和样式覆盖的问题。

* * *

## 工具类的具体应用

### 1、文本相关工具类

+   **`text-center`**：将文本对齐方式设置为居中。
+   **`text-lg`**：设置文本大小为 `lg`（大号字体）。
+   **`font-bold`**：将文本的字体加粗。
+   **`text-red-500`**：设置文本颜色为红色（`500` 是红色的一个具体深浅值）。

## 实例

<p class\="text-center text-lg font-bold text-red-500"\>Hello, Tailwind!</p\>  

### 2、背景相关工具类

+   **`bg-blue-500`**：设置元素的背景颜色为蓝色。
+   **`bg-opacity-50`**：设置背景的透明度为 50%。
+   **`bg-cover`**：将背景图像的大小调整为完全覆盖元素。

## 实例

<div class\="bg-blue-500 bg-opacity-50 p-4"\>  
  <h1 class\="text-white"\>Welcome to Tailwind</h1\>  
</div\>  

### 3、间距相关工具类

+   **`p-4`**：设置元素的内边距（padding）为 `1rem`。
+   **`m-8`**：设置元素的外边距（margin）为 `2rem`。
+   **`mt-4`**：设置元素的上外边距为 `1rem`。

## 实例

<div class\="m-8 p-4 mt-4"\>  
  <p\>This box has padding and margin.</p\>  
</div\>  

### 4、布局相关工具类

+   **`flex`**：将元素的布局模式设置为 flexbox。
+   **`grid`**：将元素的布局模式设置为 CSS Grid。
+   **`items-center`**：将 flexbox 容器中的子元素垂直居中。
+   **`justify-between`**：在 flexbox 容器中，子元素之间的空间均等分布。

## 实例

<div class\="flex items-center justify-between"\>  
  <div class\="bg-blue-500 text-white p-4"\>Item 1</div\>  
  <div class\="bg-blue-500 text-white p-4"\>Item 2</div\>  
</div\>  

### 5、边框和圆角相关工具类

+   **`border`**：添加边框。
+   **`border-2`**：设置边框宽度为 `2px`。
+   **`rounded-lg`**：设置元素的圆角为 `0.5rem`。

## 实例

<div class\="border border-2 rounded-lg p-4"\>  
  <p\>This box has a border and rounded corners.</p\>  
</div\>  

### 6、阴影相关工具类

+   **`shadow`**：为元素添加默认阴影。
+   **`shadow-lg`**：添加更大的阴影。
+   **`shadow-none`**：移除阴影。

## 实例

<div class\="shadow-lg p-6"\>  
  <p\>This box has a large shadow.</p\>  
</div\>  

### 7、响应式工具类

Tailwind 提供了响应式工具类，可以在不同的屏幕尺寸下应用不同的样式。常见的屏幕尺寸包括 `sm`（小屏幕）、`md`（中等屏幕）、`lg`（大屏幕）、`xl`（超大屏幕）。

+   **`sm:`**：仅在屏幕宽度大于或等于 640px 时生效。
+   **`md:`**：仅在屏幕宽度大于或等于 768px 时生效。
+   **`lg:`**：仅在屏幕宽度大于或等于 1024px 时生效。
+   **`xl:`**：仅在屏幕宽度大于或等于 1280px 时生效。

## 实例

<div class\="bg-blue-500 sm:bg-green-500 lg:bg-red-500 p-4"\>  
  <p\>This background color changes based on the screen size.</p\>  
</div\>  

### 8、状态工具类

Tailwind 支持交互状态的工具类，如 `hover:`, `focus:`, `active:` 等。

+   **`hover:bg-blue-700`**：在元素被鼠标悬停时，背景色变为蓝色。
+   **`focus:outline-none`**：当元素获取焦点时，去除默认的边框轮廓。
+   **`active:bg-red-500`**：在元素处于激活状态时，背景色变为红色。

## 实例

<button class\="hover:bg-blue-700 focus:outline-none active:bg-red-500"\>  
  Hover or Focus Me!  
</button\>  

### 实例

使用传统方法，自定定义 CSS 样式：

## 实例

<div class\="chat-notification"\>  
  <div class\="chat-notification-logo-wrapper"\>  
    <img class\="chat-notification-logo" src\="/img/logo.svg" alt\="ChitChat Logo"\>  
  </div\>  
  <div class\="chat-notification-content"\>  
    <h4 class\="chat-notification-title"\>ChitChat</h4\>  
    <p class\="chat-notification-message"\>You have a new message!</p\>  
  </div\>  
</div\>

<style\>  
  .chat-notification {  
    display: flex;  
    align-items: center;  
    max-width: 24rem;  
    margin: 0 auto;  
    padding: 1.5rem;  
    border-radius: 0.5rem;  
    background-color: #fff;  
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);  
  }  
  .chat-notification-logo-wrapper {  
    flex-shrink: 0;  
  }  
  .chat-notification-logo {  
    height: 3rem;  
    width: 3rem;  
  }  
  .chat-notification-content {  
    margin-left: 1.5rem;  
  }  
  .chat-notification-title {  
    color: #1a202c;  
    font-size: 1.25rem;  
    line-height: 1.25;  
  }  
  .chat-notification-message {  
    color: #718096;  
    font-size: 1rem;  
    line-height: 1.5;  
  }  
</style\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_uf1)

接下来我们看下使用 Tailwind，在 HTML 中直接使用预先存在的类来设置元素的样式，而无需编写 CSS：

## 实例

<div class\="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center gap-x-4"\>  
  <div class\="shrink-0"\>  
    <img class\="size-12" src\="/img/logo.svg" alt\="ChitChat Logo"\>  
  </div\>  
  <div\>  
    <div class\="text-xl font-medium text-black"\>ChitChat</div\>  
    <p class\="text-slate-500"\>You have a new message!</p\>  
  </div\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_uf2)

以下是对代码中每个类名的解析：

#### **外层容器：`<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center gap-x-4">`**

| **类名**           | **作用**                                               |
| ------------------ | ------------------------------------------------------ |
| **`p-6`**          | 设置元素的内边距（padding）为 1.5rem（24px）。         |
| **`max-w-sm`**     | 设置元素的最大宽度为 `sm`，对应约 24rem（384px）。     |
| **`mx-auto`**      | 设置水平外边距为 `auto`，使元素水平居中。              |
| **`bg-white`**     | 设置元素的背景颜色为白色。                             |
| **`rounded-xl`**   | 设置圆角为 `xl`，即 0.75rem（12px）。                  |
| **`shadow-lg`**    | 添加较大的阴影效果，使容器看起来有浮动感。             |
| **`flex`**         | 将元素的布局模式设置为 `flexbox`，便于子元素按行排列。 |
| **`items-center`** | 将子元素在垂直方向上居中对齐。                         |
| **`gap-x-4`**      | 设置 flex 容器中子元素之间的水平间距为 1rem（16px）。  |

#### **左侧容器：`<div class="shrink-0">`**

| **类名**       | **作用**                                                   |
| -------------- | ---------------------------------------------------------- |
| **`shrink-0`** | 禁止该元素缩小，确保其大小不受 flex 容器中其他元素的影响。 |

#### **图片：`<img class="size-12" src="/img/logo.svg" alt="ChitChat Logo">`**

| **类名**      | **作用**                                                     |
| ------------- | ------------------------------------------------------------ |
| **`size-12`** | 这不是 Tailwind 的原生类。可能是自定义类，用来设置图片大小。 |

#### **右侧内容容器：`<div>`**

无类名，作为子元素包含文本内容。

#### **标题文本：`<div class="text-xl font-medium text-black">ChitChat</div>`**

| **类名**          | **作用**                                  |
| ----------------- | ----------------------------------------- |
| **`text-xl`**     | 设置文本大小为 `xl`，即 1.25rem（20px）。 |
| **`font-medium`** | 设置字体粗细为 `medium`，即 500。         |
| **`text-black`**  | 设置文本颜色为黑色。                      |

#### **描述文本：`<p class="text-slate-500">You have a new message!</p>`**

| **类名**             | **作用**                                               |
| -------------------- | ------------------------------------------------------ |
| **`text-slate-500`** | 设置文本颜色为 `slate-500`，即石板灰色（中等深浅值）。 |