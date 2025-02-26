## Tailwind CSS 配置

Tailwind CSS 的核心配置文件为 tailwind.config.js。

tailwind.config.js 是 Tailwind CSS 的配置文件，用于定制化 Tailwind 的默认配置。

通过修改 tailwind.config.js 文件，开发者可以自定义颜色、间距、字体、断点等设计系统，满足特定项目需求。

### 创建配置文件

使用 Tailwind CSS 的 CLI 工具可以快速生成一个基础的 tailwind.config.js 文件。

在项目根目录下运行以下命令：

```
npx tailwindcss init
```

这将创建一个包含基本配置的 tailwind.config.js 文件。

### 基本结构

以下是一个典型的 tailwind.config.js 文件的结构：

## 实例

/\*\* @type {import('tailwindcss').Config} \*/  
module.exports \= {  
  content: \["./src/\*\*/\*.{html,js,vue}"\], // 定义需要扫描的模板文件路径  
  theme: {  
    extend: {}, // 自定义扩展  
  },  
  plugins: \[\], // 配置插件  
}  

以上代码告诉 Tailwind CSS 扫描 src 目录下的所有 .html, .js, 和 .vue 文件。

* * *

## 主要配置项

### 1、配置模板路径：content

在 tailwind.config.js 文件中，content 选项用于指定 Tailwind CSS 应该扫描哪些文件以收集类名。

```
content: [
  "./index.html", // 单文件路径
  "./src/**/*.{html,js,ts,jsx,tsx}", // 包含多个文件类型的路径
],
```

这将告诉 Tailwind CSS 扫描 src 目录下的所有 .html、.js、.ts\\.jsx 和 .tsx 文件。

content 字段用于指定 Tailwind 的模板文件路径，Tailwind 会扫描这些文件以生成必要的样式，减少生成的 CSS 文件体积，只生成模板文件中使用的样式，防止未使用的样式被编译到最终输出中。

### 2、自定义主题：theme

在 theme 部分，你可以定义颜色、字体、间距、边框大小等。

例如，扩展默认的颜色或添加新的颜色：

```
theme: {
  extend: {
    colors: {
      cyan: '#9cdbff',
    }
  }
}
```

这将添加一个名为 cyan 的新颜色，你可以在项目中使用 bg-cyan 这样的类名。

| **配置项**     | **描述**               | **示例**                                                     |
| -------------- | ---------------------- | ------------------------------------------------------------ |
| `fontSize`     | 自定义字体大小         | `javascript fontSize: { 'xs': '0.75rem', '4xl': '2.5rem', },` |
| `screens`      | 定义断点（响应式设计） | `javascript screens: { 'sm': '640px', 'xl': '1280px', },`    |
| `borderRadius` | 自定义圆角             | `javascript borderRadius: { 'lg': '1rem', 'xl': '1.5rem', },` |
| `extend`       | 扩展现有默认值         | `javascript extend: { colors: { danger: '#FF5A5F', }, },`    |

## 实例

theme: {  
  extend: {  
    colors: {  
      primary: '#1D4ED8',  
      secondary: '#64748B',  
    },  
    spacing: {  
      18: '4.5rem', // 新增 4.5rem 的间距  
    },  
    fontSize: {  
      '4xl': '2.5rem',  
    },  
    borderRadius: {  
      'xl': '1.5rem',  
    },  
    screens: {  
      '2xl': '1536px', // 添加新的响应式断点  
    },  
  },  
}  

通过 theme.colors 定义颜色，并在样式中引用。

```
theme: {
  extend: {
    colors: {
      brand: {
        light: '#93C5FD',
        DEFAULT: '#3B82F6',
        dark: '#1E40AF',
      },
    },
  },
}
```

## 实例

<div class\="bg-brand text-brand-light"\>Custom Colors Example</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_config1)

通过 darkMode 开启 Tailwind 的暗色模式支持。

```
module.exports = {
  darkMode: 'class', // 或 'media'
  theme: {
    extend: {
      colors: {
        background: {
          light: '#FFFFFF',
          dark: '#000000',
        },
      },
    },
  },
}
```

## 实例

<div class\="bg-background-light dark:bg-background-dark"\>  
  Dark Mode Example  
</div\>  

### 3、配置变体：variants

variants 选项允许你定义哪些状态（如 hover、focus 等）应该被包含在最终的 CSS 中。

你可以扩展或覆盖默认的变体：

```
variants: {
  extend: {
    borderColor: ['focus-visible'],
    opacity: ['disabled'],
  }
}
```

### 4、使用插件：plugins

plugins 选项允许你添加自定义的工具类。

这些插件可以是 Tailwind CSS 官方提供的，也可以是社区创建的，格式如下：

```
plugins: [
  require('some-tailwindcss-plugin')
]
```

使用插件实例：

## 实例

const plugin \= require('tailwindcss/plugin');

module.exports \= {  
  plugins: \[  
    plugin(function ({ addUtilities }) {  
      addUtilities({  
        '.text-shadow': {  
          textShadow: '2px 2px 4px rgba(0,0,0,0.5)',  
        },  
      });  
    }),  
  \],  
}

引入社区插件：

## 实例

module.exports \= {  
  plugins: \[  
    require('@tailwindcss/forms'), // 表单样式插件  
    require('@tailwindcss/typography'), // 排版插件  
  \],  
}  

* * *

## Tailwind CSS 配置

默认情况下，Tailwind 会在项目根目录中查找 tailwind.config.js 文件，您可以在其中设置自己需要的配置信息：

## 实例

/\*\* @type {import('tailwindcss').Config} \*/  
module.exports \= {  
  // 指定Tailwind CSS应该从哪些文件中提取类名。这里配置为从\`./src\`目录下所有\`.html\`和\`.js\`文件中提取。  
  content: \['./src/\*\*/\*.{html,js}'\],

  theme: {  
    // 自定义颜色配置  
    colors: {  
      'blue': '#1fb6ff', // 定义了名为'blue'的颜色，值为#1fb6ff  
      'purple': '#7e5bef', // 定义了名为'purple'的颜色，值为#7e5bef  
      'pink': '#ff49db', // 定义了名为'pink'的颜色，值为#ff49db  
      'orange': '#ff7849', // 定义了名为'orange'的颜色，值为#ff7849  
      'green': '#13ce66', // 定义了名为'green'的颜色，值为#13ce66  
      'yellow': '#ffc82c', // 定义了名为'yellow'的颜色，值为#ffc82c  
      'gray-dark': '#273444', // 定义了名为'gray-dark'的颜色，值为#273444  
      'gray': '#8492a6', // 定义了名为'gray'的颜色，值为#8492a6  
      'gray-light': '#d3dce6' // 定义了名为'gray-light'的颜色，值为#d3dce6  
    },  
    // 自定义字体族配置  
    fontFamily: {  
      sans: \['Graphik', 'sans-serif'\], // 定义了一个名为'sans'的字体族，包括'Graphik'和通用的'sans-serif'  
      serif: \['Merriweather', 'serif'\] // 定义了一个名为'serif'的字体族，包括'Merriweather'和通用的'serif'  
    },  
    // 自定义扩展配置  
    extend: {  
      // 自定义间距扩展  
      spacing: {  
        '8xl': '96rem', // 定义了一个名为'8xl'的间距，值为96rem  
        '9xl': '128rem' // 定义了一个名为'9xl'的间距，值为128rem  
      },  
      // 自定义边框圆角扩展  
      borderRadius: {  
        '4xl': '2rem' // 定义了一个名为'4xl'的边框圆角，值为2rem  
      }  
    }  
  },  
}

下表列出了 tailwind.config.js 文件的配置选项及使用说明：

| **配置项**                   | **描述**                                                     | **默认值**                                                   | **示例**                                                     |
| ---------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **content**                  | 配置 Tailwind CSS 扫描的模板文件路径，用于移除未使用的样式。 | `['./src/**/*.{html,js,ts,jsx,tsx}']`                        | `content: ["./src/**/*.html", "./src/**/*.vue"]`             |
| **theme**                    | 用于定义和扩展 Tailwind 的默认设计系统，包括颜色、间距、字体等。 | `extend: {}`                                                 | `theme: { colors: { primary: '#3490dc' } }`                  |
| **extend**                   | 用于扩展 Tailwind 默认的配置项，而不是覆盖默认值。           | `{}`                                                         | `extend: { colors: { primary: '#3490dc' } }`                 |
| **screens**                  | 配置响应式断点，决定何时应用特定的样式。                     | `{ sm: '640px', md: '768px', lg: '1024px', xl: '1280px' }`   | `screens: { '2xl': '1536px' }`                               |
| **colors**                   | 自定义或扩展颜色调色板。                                     | 默认提供一系列颜色，如 `blue`, `red`, `green` 等             | `colors: { primary: '#1D4ED8', secondary: '#64748B' }`       |
| **spacing**                  | 设置内外边距（`p`, `m`, `pt`, `mt` 等）。                    | 默认提供单位，如 `0.5rem`, `1rem`, `2rem` 等                 | `spacing: { 18: '4.5rem' }`                                  |
| **fontFamily**               | 自定义字体系列。                                             | `'sans', 'serif', 'mono'`                                    | `fontFamily: { sans: ['Inter', 'sans-serif'] }`              |
| **fontSize**                 | 自定义字体大小。                                             | `'sm': '0.875rem', 'lg': '1.125rem'`                         | `fontSize: { '4xl': '2.5rem' }`                              |
| **fontWeight**               | 自定义字体粗细。                                             | `'normal', 'bold', 'bolder', 'lighter'`                      | `fontWeight: { 'light': '300', 'bold': '700' }`              |
| **lineHeight**               | 设置行高。                                                   | `'none': '1', 'tight': '1.25', 'normal': '1.5', 'loose': '2'` | `lineHeight: { 'relaxed': '1.75', 'loose': '2' }`            |
| **borderRadius**             | 设置圆角半径。                                               | `'none': '0px', 'sm': '0.125rem', 'md': '0.375rem', 'lg': '0.5rem'` | `borderRadius: { 'xl': '1.5rem' }`                           |
| **borderWidth**              | 设置边框宽度。                                               | `{ default: '1px', '0': '0', '2': '2px' }`                   | `borderWidth: { '3': '3px' }`                                |
| **zIndex**                   | 设置 `z-index` 层级。                                        | `{ '0': '0', '10': '10', '20': '20' }`                       | `zIndex: { 'max': '9999' }`                                  |
| **opacity**                  | 设置透明度值。                                               | `{ '0': '0', '25': '0.25', '50': '0.5', '75': '0.75', '100': '1' }` | `opacity: { '40': '0.4' }`                                   |
| **boxShadow**                | 设置盒子阴影。                                               | `{ sm: '0 1px 2px 0 rgba(0, 0, 0, 0.05)', default: '0 4px 6px rgba(0, 0, 0, 0.1)'}` | `boxShadow: { 'lg': '0 10px 15px -3px rgba(0, 0, 0, 0.1)' }` |
| **container**                | 设置容器的最大宽度（用于响应式设计）。                       | `{ center: false, padding: '2rem' }`                         | `container: { center: true, padding: '1rem' }`               |
| **aspectRatio**              | 设置元素的宽高比。                                           | `{ 'none': 'none' }`                                         | `aspectRatio: { '16/9': '16/9' }`                            |
| **gridTemplateColumns**      | 设置 CSS Grid 的列模板。                                     | `{ auto: 'auto', '1fr': '1fr' }`                             | `gridTemplateColumns: { 'layout': 'repeat(3, 1fr)' }`        |
| **gridColumn**               | 设置 Grid 项的跨列行为。                                     | `{ 'span-1': 'span 1 / span 1' }`                            | `gridColumn: { 'span-2': 'span 2 / span 2' }`                |
| **transitionProperty**       | 设置过渡属性。                                               | `{ all: 'all' }`                                             | `transitionProperty: { 'color': 'color' }`                   |
| **transitionDuration**       | 设置过渡持续时间。                                           | `{ 75: '75ms', 150: '150ms', 300: '300ms' }`                 | `transitionDuration: { '400': '400ms' }`                     |
| **transitionTimingFunction** | 设置过渡时的 timing function（过渡函数）。                   | `{ 'ease': 'ease', 'linear': 'linear' }`                     | `transitionTimingFunction: { 'ease-out': 'ease-out' }`       |

通过 tailwind.config.js，可以轻松自定义 Tailwind CSS 的功能与样式，适配各种设计需求。合理利用扩展（extend）、插件（plugins）以及主题配置（theme）等特性，能够大幅提升项目的开发效率和样式灵活性。