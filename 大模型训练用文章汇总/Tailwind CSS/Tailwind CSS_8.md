## Tailwind CSS 状态处理

Tailwind CSS 提供了强大的状态类（状态修饰符），用于控制元素在不同交互状态下的样式变化。

Tailwind CSS 提供了多种状态类（如 hover:, focus:, active: 等）来帮助开发者快速处理交互效果，通过组合这些状态类，你可以非常简便地实现悬停、聚焦、点击等状态下的样式变化，提高用户体验。

状态类的前缀:

| **状态**   | **前缀**        | **作用**                                                     |
| ---------- | --------------- | ------------------------------------------------------------ |
| 悬停状态   | `hover:`        | 控制元素在鼠标悬停时的样式变化                               |
| 聚焦状态   | `focus:`        | 控制元素在获得焦点时的样式变化                               |
| 激活状态   | `active:`       | 控制元素在被点击时的样式变化                                 |
| 访问状态   | `visited:`      | 控制访问过的链接的样式变化                                   |
| 焦点内状态 | `focus-within:` | 控制父元素在其子元素获得焦点时的样式变化                     |
| 各状态组合 | 无特定前缀      | 可以同时组合多个状态前缀，如 `hover:`, `focus:`，以及 `active:` |

### 1\. 悬停（Hover）

悬停（`hover`）状态是指当用户将鼠标悬停在一个元素上时，元素的样式发生变化。使用 `hover:` 前缀，可以轻松实现这一效果。

**语法**：

```
hover:{class}
```

例如，`hover:bg-sky-700` 会在鼠标悬停时将元素的背景颜色更改为 `sky-700`。

**常见用法**：

## 实例

<button class\="px-4 py-2 bg-blue-500 text-white hover:bg-sky-700"\>  
  鼠标移动到这  
</button\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state1)

当鼠标悬停时，按钮背景色从 `blue-500` 变为 `sky-700`。

**更多例子**：

+   `hover:text-white`: 悬停时将文本颜色变为白色。
+   `hover:underline`: 悬停时为文本添加下划线。
+   `hover:border-2 hover:border-gray-500`: 悬停时增加 2px 的边框，并设置为灰色。

### 2\. 聚焦（Focus）

聚焦（`focus`）状态指的是当用户与表单元素（如输入框）交互时，元素会获得焦点。使用 `focus:` 前缀，可以控制元素在聚焦时的样式。

**语法**：

```
focus:{class}
```

例如，`focus:ring-2 focus:ring-blue-600` 会在元素获得焦点时显示一个蓝色的环。

## 实例

<input class\="border p-2 focus:outline-none focus:ring-2 focus:ring-blue-600" type\="text" placeholder\="点击我聚焦!"\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state2)

当用户点击或选中输入框时，输入框会显示一个蓝色的高亮环。

**更多例子**：

+   `focus:text-black`: 聚焦时将文本颜色变为黑色。
+   `focus:border-blue-500`: 聚焦时将输入框的边框颜色变为蓝色。
+   `focus:ring-4 focus:ring-opacity-50 focus:ring-green-500`: 聚焦时显示一个绿色的环，高亮显示，并设置透明度。

### 3\. 活动（Active）

活动（`active`）状态是指当元素被用户点击时，元素的样式会发生变化。使用 `active:` 前缀可以控制点击时的样式。

**语法**：

```
active:{class}
```

例如，`active:bg-green-700` 会在元素被按下时更改背景颜色为绿色。

**常见用法**：

## 实例

<button class\="px-4 py-2 bg-blue-500 text-white active:bg-green-700"\>  
  点我  
</button\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state3)

当按钮被按下时，背景色会变为绿色 `green-700`。

**更多例子**：

+   `active:text-gray-600`: 点击时将文本颜色变为灰色。
+   `active:ring-2 active:ring-opacity-50 active:ring-green-500`: 点击时为元素添加绿色的环形高亮效果。

### 4\. 组合状态

Tailwind CSS 支持组合多个状态修饰符，使得你可以更精确地控制交互状态下的样式变化。例如，你可以结合悬停、焦点、活动状态以及响应式或暗色模式。

**语法**：

```
{state}:{class}
```

例如，`dark:md:hover:bg-fuchsia-600` 会在黑暗模式下、中等断点时、悬停时更改背景颜色。

## 实例

<button class\="px-4 py-2 bg-blue-500 text-white hover:bg-sky-700 focus:outline-none dark:hover:bg-fuchsia-600"\>  
  鼠标悬停或聚焦我  
</button\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state4)

在常规模式下，按钮背景颜色会在悬停时变为 `sky-700`，而在暗色模式下，背景色会变为 `fuchsia-600`。

**更多例子**：

+   `sm:focus:ring-2`: 在小屏幕设备下，当元素获得焦点时，添加一个 2px 的高亮环。
+   `lg:active:bg-red-500`: 在大屏幕设备下，点击按钮时改变背景色为红色。

### 5\. 伪类（Pseudo-classes）

Tailwind CSS 还支持多种伪类修饰符，允许你根据元素在文档中的位置或顺序来应用样式。

**常见伪类修饰符**：

+   `first-child`: 作用于第一个子元素。
+   `last-child`: 作用于最后一个子元素。
+   `odd-child`: 作用于奇数位置的子元素。
+   `even-child`: 作用于偶数位置的子元素。

## 实例

<ul class\="space-y-4"\>  
  <li class\="first:font-bold last:font-light"\>Item 1</li\>  
  <li class\="odd:bg-gray-100"\>Item 2</li\>  
  <li class\="even:bg-gray-200"\>Item 3</li\>  
</ul\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state5)

+   第一个列表项 `Item 1` 会加粗，最后一个列表项 `Item 3` 会变为更轻的字体。
+   奇数和偶数项会根据不同背景颜色来区分。

### 6\. 表单状态（Form States）

Tailwind CSS 提供了一些表单状态类，用于控制表单元素在不同状态下的样式变化，如必填（`required`）、无效（`invalid`）和禁用（`disabled`）状态。

**常见类**：

+   `required`: 表示输入字段为必填项。
+   `invalid`: 用于无效的表单输入。
+   `disabled`: 禁用的表单元素。

## 实例

<input class\="border p-2 required:border-red-500 invalid:border-yellow-500 disabled:bg-gray-300" type\="text" placeholder\="输入内容"\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state6)

+   如果输入框无效，会显示黄色边框。
+   如果输入框被禁用，背景色将变为灰色。

* * *

### 7\. 基于父状态的样式（Group Modifier）

Tailwind CSS 允许在父元素悬停或聚焦时影响子元素的样式。通过 `group-hover` 和 `group-focus` 修饰符，你可以在父元素状态变化时调整子元素的样式。

**语法**：

```
group-{state}:{class}
```

例如，`group-hover:bg-gray-300` 会在父元素悬停时，应用子元素的背景颜色变为灰色。

## 实例

<div class\="group"\>  
  <button class\="px-4 py-2 bg-blue-500 text-white group-hover:bg-gray-300"\>  
    将鼠标悬停在父级上  
  </button\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state7)

当父容器被悬停时，按钮背景色会变为灰色。

### 8\. 响应式和暗色模式

Tailwind CSS 允许你结合响应式前缀和暗色模式修饰符，在不同的屏幕尺寸和模式下应用不同的样式。

**语法**：

+   响应式前缀：`sm:`, `md:`, `lg:`, `xl:`, `2xl:`
+   暗色模式前缀：`dark:`

## 实例

<button class\="px-4 py-2 bg-blue-500 text-white dark:bg-gray-800 sm:hover:bg-blue-700 md:focus:ring-2 md:focus:ring-blue-500"\>  
  响应式和深色模式按钮  
</button\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state8)

在小屏幕时，悬停时背景色会变为 `blue-700`，在中等屏幕时，聚焦时会添加蓝色的高亮环，而在暗色模式下，背景颜色会变为灰色。

### 9\. 配置变体（Variants）

在 `tailwind.config.js` 文件中，可以通过 `variants` 部分配置启用哪些状态变体。这样，你可以根据项目需要启用或禁用特定状态下的样式变化。

## 实例

module.exports \= {  
  theme: {  
    extend: {},  
  },  
  variants: {  
    extend: {  
      backgroundColor: \['active', 'group-hover'\],  
      textColor: \['focus-visible', 'disabled'\],  
    },  
  },  
}  

在这个配置中，`backgroundColor` 增加了 `active` 和 `group-hover` 状态，而 `textColor` 增加了 `focus-visible` 和 `disabled` 状态。

### 10、第一个、最后一个、奇数和偶数

当元素是第一个子元素或最后一个元素时，使用 first 和 last 修饰符来设置元素的样式：

## 实例

<ul class\="space-y-2"\>  
  <li class\="first:text-red-500"\>First item</li\>  
  <li\>Second item</li\>  
  <li class\="last:font-bold"\>Last item</li\>  
</ul\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state9)

效果：

+   第一个列表项的文本颜色变为红色 text-red-500。
+   最后一个列表项的字体变为加粗 font-bold。

odd 修饰符：odd 用于选择父容器中所有奇数位置的子元素（基于 1 开始的索引）。

## 实例

<ul class\="space-y-2"\>  
  <li class\="odd:bg-gray-100"\>Item 1</li\>  
  <li\>Item 2</li\>  
  <li class\="odd:bg-gray-100"\>Item 3</li\>  
  <li\>Item 4</li\>  
</ul\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state10)

**效果：**列表中的第 1 项和第 3 项的背景颜色变为浅灰色 bg-gray-100。

even 修饰符：even 用于选择父容器中所有偶数位置的子元素（基于 1 开始的索引）。

## 实例

<ul class\="space-y-2"\>  
  <li\>Item 1</li\>  
  <li class\="even:bg-gray-200"\>Item 2</li\>  
  <li\>Item 3</li\>  
  <li class\="even:bg-gray-200"\>Item 4</li\>  
</ul\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_state11)

**效果：**列表中的第 2 项和第 4 项的背景颜色变为较深的灰色 bg-gray-200。

### 修饰符参考

| **Modifier**   | **CSS 对应伪类/伪元素或规则**                    | **说明**                           | **示例代码**                                                 |
| -------------- | ------------------------------------------------ | ---------------------------------- | ------------------------------------------------------------ |
| `hover`        | `:hover`                                         | 鼠标悬停时生效                     | `<button class="hover:bg-blue-500">Hover me</button>`        |
| `focus`        | `:focus`                                         | 元素获得焦点时生效                 | `<input class="focus:ring-2 focus:ring-blue-600" />`         |
| `focus-within` | `:focus-within`                                  | 父容器内的任意子元素获得焦点时生效 | `<div class="focus-within:border-blue-500"><input /></div>`  |
| `active`       | `:active`                                        | 元素被按下或处于活动状态时生效     | `<button class="active:bg-green-700">Click me</button>`      |
| `visited`      | `:visited`                                       | 已访问的链接                       | `<a class="visited:text-purple-600" href="#">Visited link</a>` |
| `target`       | `:target`                                        | 目标链接被激活时生效               | `<div id="section" class="target:bg-yellow-500"></div>`      |
| `first`        | `:first-child`                                   | 第一个子元素                       | `<ul><li class="first:text-red-500">First</li><li>Other</li></ul>` |
| `last`         | `:last-child`                                    | 最后一个子元素                     | `<ul><li>Other</li><li class="last:font-bold">Last</li></ul>` |
| `odd`          | `:nth-child(odd)`                                | 奇数子元素（从 1 开始计数）        | `<ul><li class="odd:bg-gray-100">Odd</li><li>Even</li></ul>` |
| `even`         | `:nth-child(even)`                               | 偶数子元素                         | `<ul><li>Odd</li><li class="even:bg-gray-200">Even</li></ul>` |
| `empty`        | `:empty`                                         | 内容为空的元素                     | `<div class="empty:bg-gray-50"></div>`                       |
| `disabled`     | `:disabled`                                      | 被禁用的表单元素                   | `<button class="disabled:opacity-50" disabled>Disabled</button>` |
| `enabled`      | `:enabled`                                       | 启用状态的表单元素                 | `<input class="enabled:border-blue-500" />`                  |
| `checked`      | `:checked`                                       | 被选中的复选框或单选按钮           | `<input type="checkbox" class="checked:bg-blue-500" checked />` |
| `required`     | `:required`                                      | 表单元素为必填项                   | `<input class="required:border-red-500" required />`         |
| `before`       | `::before`                                       | 在元素前插入的伪元素               | `<div class="before:content-['*'] before:text-red-500"></div>` |
| `after`        | `::after`                                        | 在元素后插入的伪元素               | `<div class="after:content-['!'] after:text-green-500"></div>` |
| `sm`           | `@media (min-width: 640px)`                      | 小屏幕（640px 起）                 | `<div class="sm:bg-blue-100">Resize to small screen</div>`   |
| `dark`         | `@media (prefers-color-scheme: dark)`            | 暗黑模式                           | `<div class="dark:bg-black dark:text-white">Dark mode content</div>` |
| `rtl`          | `[dir="rtl"]`                                    | 右到左文本方向                     | `<div dir="rtl" class="rtl:text-right">Right to Left</div>`  |
| `aria-checked` | `[aria-checked="true"]`                          | 对具有 ARIA 属性的元素应用样式     | `<div aria-checked="true" class="aria-checked:bg-green-500">Checked</div>` |
| `motion-safe`  | `@media (prefers-reduced-motion: no-preference)` | 动画偏好设置：无偏好时生效         | `<div class="motion-safe:transition-transform motion-safe:duration-500"></div>` |

