+ ## Tailwind CSS 背景颜色

  在 Tailwind CSS 中，**背景颜色**（Background Color）是最常用的工具类之一，它允许你快速为元素设置背景颜色。

  Tailwind 提供了多种颜色选项以及不同的色调，确保你能灵活地应用所需的样式。

  **背景颜色基本语法**：

  ```
  <div class="bg-{color}">
    <!-- 内容 -->
  </div>
  ```

  **常见的背景颜色类**：

  | 类名             | 描述                                                     | 例子                         |
  | ---------------- | -------------------------------------------------------- | ---------------------------- |
  | `bg-{color}`     | 设置背景颜色                                             | `bg-red-500`，`bg-blue-200`  |
  | `bg-transparent` | 设置透明背景颜色                                         | `bg-transparent`             |
  | `bg-current`     | 设置背景颜色为当前文本颜色（常用于图标的背景）           | `bg-current`                 |
  | `bg-white`       | 设置背景颜色为白色                                       | `bg-white`                   |
  | `bg-black`       | 设置背景颜色为黑色                                       | `bg-black`                   |
  | `bg-gray-{n}`    | 设置背景颜色为灰色，`{n}` 为灰色的深浅度（从 50 到 900） | `bg-gray-100`, `bg-gray-700` |

  **背景颜色的渐变（Gradient）**：

  Tailwind CSS 支持背景的线性渐变、径向渐变等。你可以使用 `bg-gradient-to-{direction}` 来指定渐变的方向，并使用 `from-{color}`、`to-{color}` 来设置渐变的起始颜色和结束颜色。

  | 类名                         | 描述                                                         | 例子                              |
  | ---------------------------- | ------------------------------------------------------------ | --------------------------------- |
  | `bg-gradient-to-{direction}` | 设置渐变背景的方向，`direction` 可以是 `t`、`r`、`b`、`l`、`tr`、`tl`、`br`、`bl`等 | `bg-gradient-to-r` (从左到右渐变) |
  | `from-{color}`               | 设置渐变背景的起始颜色                                       | `from-blue-500`                   |
  | `to-{color}`                 | 设置渐变背景的结束颜色                                       | `to-green-300`                    |
  | `via-{color}`                | 设置渐变中间的颜色（可选）                                   | `via-purple-400`                  |

  ## 实例

  <div class\="bg-gradient-to-r from-blue-500 to-green-300 p-10 text-white"\>  
    渐变背景从蓝色到绿色  
  </div\>  

  **背景颜色透明度**（Opacity）：

  Tailwind 也提供了控制背景透明度的工具类，使用 `bg-opacity-{value}` 来设置透明度值，`{value}` 从 0 到 100 的整数表示透明度的百分比。

  | 类名             | 描述                   | 例子             |
  | ---------------- | ---------------------- | ---------------- |
  | `bg-opacity-{n}` | 设置背景颜色的透明度   | `bg-opacity-50`  |
  | `bg-opacity-0`   | 设置背景颜色完全透明   | `bg-opacity-0`   |
  | `bg-opacity-100` | 设置背景颜色完全不透明 | `bg-opacity-100` |

  ## 实例

  <div class\="bg-blue-500 bg-opacity-50 p-10 text-white"\>  
    背景为半透明的蓝色  
  </div\>  

  **使用 Tailwind 配置中的自定义背景颜色**：

  你可以在 `tailwind.config.js` 配置文件中自定义背景颜色。通过在 `theme.extend` 部分的 `colors` 属性下定义颜色，你可以扩展默认的颜色集。

  ## 实例

  module.exports \= {  
    theme: {  
      extend: {  
        colors: {  
          'custom-blue': '#1D4ED8',  
          'custom-gray': '#4B5563',  
        }  
      }  
    }  
  }  

  在 HTML 中使用自定义背景颜色：

  ## 实例

  <div class\="bg-custom-blue p-10 text-white"\>  
    使用自定义蓝色背景  
  </div\>  

  ### **综合实例**

  ## 实例

  <!-- 背景颜色实例 -->  
  <div class\="bg-blue-500 text-white p-6 mb-6"\>  
      <h1 class\="text-xl"\>蓝色背景</h1\>  
      <p\>这是一个拥有蓝色背景的容器，文字颜色为白色。</p\>  
  </div\>

  <!-- 渐变背景实例 -->  
  <div class\="bg-gradient-to-r from-purple-500 via-pink-500 to-red-500 text-white p-6 mb-6"\>  
      <h1 class\="text-xl"\>渐变背景</h1\>  
      <p\>这是一个线性渐变背景，从紫色到粉色再到红色。</p\>  
  </div\>

  <!-- 背景透明度实例 -->  
  <div class\="bg-green-500 bg-opacity-50 text-white p-6"\>  
      <h1 class\="text-xl"\>透明度背景</h1\>  
      <p\>这是一个具有半透明绿色背景的容器。</p\>  
  </div\>

  [尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_bg1)

  **解析：**

  **基本背景颜色**：

  +   `bg-blue-500`：设置背景颜色为蓝色。
  +   `text-white`：设置文本颜色为白色。

  **渐变背景**：

  +   `bg-gradient-to-r`：设置渐变背景的方向为从左到右。
  +   `from-purple-500`：设置渐变的起始颜色为紫色。
  +   `to-red-500`：设置渐变的结束颜色为红色。

  **背景透明度**：

  +   `bg-opacity-50`：设置背景颜色的透明度为 50%（半透明）。