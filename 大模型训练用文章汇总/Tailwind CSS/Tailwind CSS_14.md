## Tailwind CSS 布局类

Tailwind CSS 提供了丰富的布局相关类，允许开发者以极其灵活的方式控制页面的各个方面。

接下来，我们将详细解释一些关键的布局相关类。

### 1、宽高比 (Aspect Ratio)

Aspect Ratio 类可以帮助你设置元素的宽高比，避免在响应式设计中元素拉伸或压缩。

**主要类：**

| 类名            | CSS属性及值             | 描述                                                         |
| --------------- | ----------------------- | ------------------------------------------------------------ |
| `aspect-auto`   | `aspect-ratio: auto;`   | 这个类会让元素保持其自然宽高比，不进行任何强制调整。适用于你想要元素根据内容自动调整大小，而不是强制填充或缩小到特定的宽高比。 |
| `aspect-square` | `aspect-ratio: 1 / 1;`  | 这个类会强制元素的宽高比为1:1，即宽度和高度相等，常用于创建正方形或圆形的元素。 |
| `aspect-video`  | `aspect-ratio: 16 / 9;` | 这个类会强制元素的宽高比为16:9，这是一种常见的视频宽高比，适用于需要显示视频或模拟视频播放器的元素。 |

## 实例

<!-- 保持 16:9 的宽高比 -->  
<div class\="aspect-ratio"\>  
  <img src\="video.jpg" alt\="Video" class\="object-cover"\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout1)

### 2、容器 (Container)

Container 类可以使容器元素响应式地适应不同屏幕大小，常用于设置内容的最大宽度。

**主要类：**

+   `container`：使元素成为一个响应式容器。
+   `mx-auto`：使容器水平居中。

| 类名            | CSS属性及值          | 描述                                               |
| --------------- | -------------------- | -------------------------------------------------- |
| `container`     | `width: 100%;`       | 容器宽度默认为100%，占据整个父元素的宽度。         |
| `sm:container`  | `max-width: 640px;`  | 在屏幕宽度大于等于640px时，容器最大宽度为640px。   |
| `md:container`  | `max-width: 768px;`  | 在屏幕宽度大于等于768px时，容器最大宽度为768px。   |
| `lg:container`  | `max-width: 1024px;` | 在屏幕宽度大于等于1024px时，容器最大宽度为1024px。 |
| `xl:container`  | `max-width: 1280px;` | 在屏幕宽度大于等于1280px时，容器最大宽度为1280px。 |
| `2xl:container` | `max-width: 1536px;` | 在屏幕宽度大于等于1536px时，容器最大宽度为1536px。 |

使用这些类时，你可以创建具有响应式最大宽度的容器，这在创建布局时非常有用，尤其是当你想要限制内容的宽度以提高可读性时。

## 实例

<div class\="container mx-auto"\>  
  <!-- 内容 -->  
</div\>

<div class\="lg:container mx-auto"\>  
  <!-- 在大屏幕上宽度最大为1024px的内容 -->  
</div\>

在这些例子中，第一个`<div>`将始终占据100%的宽度，而第二个`<div>`在大屏幕（`lg`）及以上的屏幕尺寸时，其最大宽度将被限制为1024px。`mx-auto`类用于水平居中容器。

### 3、列布局 (Columns)

Columns 类用于实现多列布局。

你可以控制列数以及列之间的间距。

**主要类：**

+   `columns-{n}`：设置列的数量。
+   `space-x-{size}`：设置列之间的间距。

| 类名           | CSS属性及值                   | 描述                                       |
| -------------- | ----------------------------- | ------------------------------------------ |
| `columns-1`    | `columns: 1;`                 | 设置元素的列数为1。                        |
| `columns-2`    | `columns: 2;`                 | 设置元素的列数为2。                        |
| `columns-3`    | `columns: 3;`                 | 设置元素的列数为3。                        |
| `columns-4`    | `columns: 4;`                 | 设置元素的列数为4。                        |
| `columns-5`    | `columns: 5;`                 | 设置元素的列数为5。                        |
| `columns-6`    | `columns: 6;`                 | 设置元素的列数为6。                        |
| `columns-7`    | `columns: 7;`                 | 设置元素的列数为7。                        |
| `columns-8`    | `columns: 8;`                 | 设置元素的列数为8。                        |
| `columns-9`    | `columns: 9;`                 | 设置元素的列数为9。                        |
| `columns-10`   | `columns: 10;`                | 设置元素的列数为10。                       |
| `columns-11`   | `columns: 11;`                | 设置元素的列数为11。                       |
| `columns-12`   | `columns: 12;`                | 设置元素的列数为12。                       |
| `columns-auto` | `columns: auto;`              | 设置元素的列数自动，根据内容自动调整列宽。 |
| `columns-3xs`  | `columns: 16rem; /* 256px */` | 设置元素的列宽为16rem（256px）。           |
| `columns-2xs`  | `columns: 18rem; /* 288px */` | 设置元素的列宽为18rem（288px）。           |
| `columns-xs`   | `columns: 20rem; /* 320px */` | 设置元素的列宽为20rem（320px）。           |
| `columns-sm`   | `columns: 24rem; /* 384px */` | 设置元素的列宽为24rem（384px）。           |
| `columns-md`   | `columns: 28rem; /* 448px */` | 设置元素的列宽为28rem（448px）。           |
| `columns-lg`   | `columns: 32rem; /* 512px */` | 设置元素的列宽为32rem（512px）。           |
| `columns-xl`   | `columns: 36rem; /* 576px */` | 设置元素的列宽为36rem（576px）。           |
| `columns-2xl`  | `columns: 42rem; /* 672px */` | 设置元素的列宽为42rem（672px）。           |
| `columns-3xl`  | `columns: 48rem; /* 768px */` | 设置元素的列宽为48rem（768px）。           |
| `columns-4xl`  | `columns: 56rem; /* 896px */` | 设置元素的列宽为56rem（896px）。           |
| `columns-5xl`  | \`columns: 64rem; /\*         |                                            |

## 实例

<!-- 创建 3 列的布局 -->  
<div class\="columns-3 space-x-4"\>  
  <p\>Column 1</p\>  
  <p\>Column 2</p\>  
  <p\>Column 3</p\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout2)

### 4、分页

以下类可以帮助开发者更好地控制文档的分页和分栏布局，以提高打印输出的可读性和美观性。

**主要类：**

+   `break-after-{value}`：控制分页后的行为。
+   `break-before-{value}`：控制分页前的行为。
+   `break-inside-{value}`：控制元素内部分页的行为。

| 类名                     | CSS属性及值                | 描述                                                         |
| ------------------------ | -------------------------- | ------------------------------------------------------------ |
| `break-after-auto`       | `break-after: auto;`       | 允许内容在该元素后自然分页或分列。                           |
| `break-after-avoid`      | `break-after: avoid;`      | 尽量避免在该元素后进行分页或分列。                           |
| `break-after-all`        | `break-after: all;`        | 强制在该元素后进行分页或分列，即使它不是分页或分列的自然位置。 |
| `break-after-avoid-page` | `break-after: avoid-page;` | 尽量避免在该元素后进行分页，但允许分列。                     |
| `break-after-page`       | `break-after: page;`       | 强制在该元素后进行分页，但不允许分列。                       |
| `break-after-left`       | `break-after: left;`       | 强制在该元素后进行分页或分列，优先选择左侧页面。             |
| `break-after-right`      | `break-after: right;`      | 强制在该元素后进行分页或分列，优先选择右侧页面。             |
| `break-after-column`     | `break-after: column;`     | 强制在该元素后进行分列，但不允许分页。                       |

以上类用于控制内容在打印或分栏布局中的分页或分列行为：

+   break-after-auto 允许浏览器决定是否在元素后进行分页或分列。
+   break-after-avoid 则告诉浏览器尽量避免在该元素后进行分页或分列。

| 类名                      | CSS属性及值                 | 描述                                                         |
| ------------------------- | --------------------------- | ------------------------------------------------------------ |
| `break-before-auto`       | `break-before: auto;`       | 允许内容在该元素前自然分页或分列。                           |
| `break-before-avoid`      | `break-before: avoid;`      | 尽量避免在该元素前进行分页或分列。                           |
| `break-before-all`        | `break-before: all;`        | 强制在该元素前进行分页或分列，即使它不是分页或分列的自然位置。 |
| `break-before-avoid-page` | `break-before: avoid-page;` | 尽量避免在该元素前进行分页，但允许分列。                     |
| `break-before-page`       | `break-before: page;`       | 强制在该元素前进行分页，但不允许分列。                       |
| `break-before-left`       | `break-before: left;`       | 强制在该元素前进行分页或分列，优先选择左侧页面。             |
| `break-before-right`      | `break-before: right;`      | 强制在该元素前进行分页或分列，优先选择右侧页面。             |
| `break-before-column`     | `break-before: column;`     | 强制在该元素前进行分列，但不允许分页。                       |

以上类用于控制内容在打印或分栏布局中的分页或分列行为。

+   break-before-auto 允许浏览器决定是否在元素前进行分页或分列。
+   break-before-avoid 则告诉浏览器尽量避免在元素前进行分页或分列。

| 类名                        | CSS属性及值                   | 描述                                       |
| --------------------------- | ----------------------------- | ------------------------------------------ |
| `break-inside-auto`         | `break-inside: auto;`         | 允许内容在该元素内部自然分页或分列。       |
| `break-inside-avoid`        | `break-inside: avoid;`        | 尽量避免在该元素内部进行分页或分列。       |
| `break-inside-avoid-page`   | `break-inside: avoid-page;`   | 尽量避免在该元素内部进行分页，但允许分列。 |
| `break-inside-avoid-column` | `break-inside: avoid-column;` | 尽量避免在该元素内部进行分列，但允许分页。 |

以上类用于控制内容在打印或分栏布局中是否允许在元素内部进行分页或分列。

+   break-inside-auto 允许浏览器决定是否在元素内部进行分页或分列。
+   break-inside-avoid 则告诉浏览器尽量避免在元素内部进行分页或分列。

## 实例

<div class\="columns-2"\>  
  <p\>好吧，让我告诉你一些事情，...</p\>  
  <p class\="break-after-column"\>当然，继续我们的内容...</p\>  
  <p\>也许我们可以...</p\>  
  <p\>如果你认为这是...</p\>  
</div\>  

在这个例子中，`<div>` 元素被设置为两列布局（`columns-2`），其中包含四个 `<p>` 段落。第二个 `<p>` 段落有一个 `break-after-column` 类，这会强制在该段落后进行分列，但不允许分页。这意味着如果内容足够多，第二个段落后的内容将开始一个新的列，而不是继续在同一列的下一行。其他段落则没有特别的分列指令，它们将根据内容自然流动。

### 5、文本断行

以下是 Tailwind CSS 中用于控制元素片段如何在多行、多列或多页中渲染的工具类及其对应的 CSS 属性：

| 类名                   | CSS属性及值                    | 描述                                                         |
| ---------------------- | ------------------------------ | ------------------------------------------------------------ |
| `box-decoration-clone` | `box-decoration-break: clone;` | 指定当一个盒子被分割成多个盒子时（例如，在列或页的边界上），每个盒子应该克隆原始盒子的装饰（边框、背景等）。 |
| `box-decoration-slice` | `box-decoration-break: slice;` | 指定当一个盒子被分割成多个盒子时，每个盒子应该"切割"原始盒子的装饰，使得装饰在每个盒子中连续显示。 |

以上类用于控制元素的装饰（如边框和背景）在多列布局或分页时的表现。

+   box-decoration-clone 会使得每个盒子片段都显示完整的装饰。
+   box-decoration-slice 则会在盒子被分割的地方"切割"装饰，使得装饰在视觉上保持连续。

这些工具类可以帮助开发者更好地控制元素在复杂布局中的视觉效果。

## 实例

<span class\="box-decoration-slice bg-gradient-to-r from-indigo-600 to-pink-500 text-white px-2 ..."\>  
  Hello<br /\>  
  World  
</span\>  
<span class\="box-decoration-clone bg-gradient-to-r from-indigo-600 to-pink-500 text-white px-2 ..."\>  
  Hello<br /\>  
  World  
</span\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout3)

### 6、盒子大小

Tailwind CSS 提供了两个工具类来控制元素的盒模型（box-sizing）：

+   `box-border`：包括内边距和边框在内计算元素的总尺寸。
+   `box-content`：不包括内边距和边框，计算元素的尺寸。

**1、box-border**

CSS 属性:

```
box-sizing: border-box;
```

使用 box-border 工具类设置元素的 box-sizing 属性为 border-box。这意味着当你给元素指定高度或宽度时，浏览器会将元素的边框和内边距包含在内。

如果一个元素的尺寸是 100px × 100px，并且有 2px 的边框和 4px 的内边距，那么元素的总渲染尺寸将是 112px × 112px。

![](https://www.runoob.com/wp-content/uploads/2024/12/94822aa0c52ab0973d11855350af5a78.png)

## 实例

<div class\="box-content h-32 w-32 p-4 border-4 ..."\>  
  <!-- ... -->  
</div\>  

**2、box-content**

CSS 属性:

```
box-sizing: content-box;
```

使用 box-content 工具类设置元素的 box-sizing 属性为 content-box。这意味着浏览器会在元素指定的宽度或高度之外添加边框和内边距。

如果一个元素的尺寸是 100px × 100px，并且有 2px 的边框和 4px 的内边距，那么元素的实际渲染尺寸将是 112px × 112px，内部内容区域为 100px × 100px。

![](https://www.runoob.com/wp-content/uploads/2024/12/a78a6786c2fc33c8eec879c7ed2374b7.png)

## 实例

<div class\="box-content h-32 w-32 p-4 border-4 ..."\>  
  <!-- ... -->  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout4)

### display 属性

display 属性用于控制元素的显示类型，决定元素如何在页面中展示。

| Tailwind 类名        | CSS 属性及值                   | 描述                                                         |
| -------------------- | ------------------------------ | ------------------------------------------------------------ |
| `block`              | `display: block;`              | 将元素显示为块级元素，它会独占一行。                         |
| `inline-block`       | `display: inline-block;`       | 将元素显示为行内块级元素，可以在行内显示并拥有自己的宽度和高度。 |
| `inline`             | `display: inline;`             | 将元素显示为行内元素，它会与其他行内元素并排显示。           |
| `flex`               | `display: flex;`               | 将元素显示为弹性容器，允许使用 Flexbox 布局。                |
| `inline-flex`        | `display: inline-flex;`        | 将元素显示为行内弹性容器，允许使用 Flexbox 布局。            |
| `table`              | `display: table;`              | 将元素显示为表格元素。                                       |
| `inline-table`       | `display: inline-table;`       | 将元素显示为行内表格元素。                                   |
| `table-caption`      | `display: table-caption;`      | 将元素显示为表格标题。                                       |
| `table-cell`         | `display: table-cell;`         | 将元素显示为表格单元格。                                     |
| `table-column`       | `display: table-column;`       | 将元素显示为表格列。                                         |
| `table-column-group` | `display: table-column-group;` | 将元素显示为表格列组。                                       |
| `table-footer-group` | `display: table-footer-group;` | 将元素显示为表格页脚组。                                     |
| `table-header-group` | `display: table-header-group;` | 将元素显示为表格头部组。                                     |
| `table-row-group`    | `display: table-row-group;`    | 将元素显示为表格行组。                                       |
| `table-row`          | `display: table-row;`          | 将元素显示为表格行。                                         |
| `flow-root`          | `display: flow-root;`          | 将元素显示为流根元素，这是一个 BFC（块级格式化上下文）。     |
| `grid`               | `display: grid;`               | 将元素显示为网格容器，允许使用 CSS Grid 布局。               |
| `inline-grid`        | `display: inline-grid;`        | 将元素显示为行内网格容器，允许使用 CSS Grid 布局。           |
| `contents`           | `display: contents;`           | 将元素的盒子模型移除，使其子元素直接显示在其位置。           |
| `list-item`          | `display: list-item;`          | 将元素显示为列表项。                                         |
| `hidden`             | `display: none;`               | 将元素隐藏，不显示在页面上。                                 |

## 实例

<div class\="relative rounded-xl overflow-auto"\>  
    <div class\="mx-auto max-w-xs bg-white shadow-xl p-4 text-slate-500 text-sm leading-6 sm:text-base sm:leading-7 dark:bg-slate-800 dark:text-slate-400"\>  
    当控制文本流时，使用 CSS 属性  
    <span class\="inline bg-sky-100 font-bold text-sm text-slate-900 font-mono rounded dark:bg-slate-600 dark:text-slate-200"\>display: inline</span\>  
    将使得元素内的文本正常换行。  
    <br\>  
    <br\>  
    而使用属性 <span class\="inline-block bg-sky-100 font-bold text-sm text-slate-900 font-mono rounded dark:bg-slate-600 dark:text-slate-200"\>display: inline-block</span\>  
    将包裹元素，防止其内部文本扩展超出其父元素。  
    <br\>  
    <br\>  
    最后，使用属性 <span class\="block bg-sky-100 font-bold text-sm text-slate-900 font-mono rounded dark:bg-slate-600 dark:text-slate-200"\>display: block</span\>  
    将使元素独占一行并填充其父元素。  
    </div\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout5)

使用 table、table-row、table-cell、table-caption、table-column、table-column-group、table-header-group、table-row-group 和 table-footer-group 工具类来创建表现得像它们各自对应表格元素的元素。

## 实例

<div class\="table w-full ..."\>  
  <div class\="table-header-group ..."\>  
    <div class\="table-row"\>  
      <div class\="table-cell text-left ..."\>Song</div\>  
      <div class\="table-cell text-left ..."\>Artist</div\>  
      <div class\="table-cell text-left ..."\>Year</div\>  
    </div\>  
  </div\>  
  <div class\="table-row-group"\>  
    <div class\="table-row"\>  
      <div class\="table-cell ..."\>The Sliding Mr. Bones (Next Stop, Pottersville)</div\>  
      <div class\="table-cell ..."\>Malcolm Lockyer</div\>  
      <div class\="table-cell ..."\>1961</div\>  
    </div\>  
    <div class\="table-row"\>  
      <div class\="table-cell ..."\>Witchy Woman</div\>  
      <div class\="table-cell ..."\>The Eagles</div\>  
      <div class\="table-cell ..."\>1972</div\>  
    </div\>  
    <div class\="table-row"\>  
      <div class\="table-cell ..."\>Shining Star</div\>  
      <div class\="table-cell ..."\>Earth, Wind, and Fire</div\>  
      <div class\="table-cell ..."\>1975</div\>  
    </div\>  
  </div\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout6)

### 浮动

float-\* 控制元素浮动的位置，通常用于环绕文本。

主要类：

| Tailwind 类名 | CSS 属性及值           | 描述                                                         |
| ------------- | ---------------------- | ------------------------------------------------------------ |
| `float-start` | `float: inline-start;` | 使元素浮动到其包含块的起始位置。在 LTR（左至右）语言中，这通常是左边；在 RTL（右至左）语言中，这通常是右边。 |
| `float-end`   | `float: inline-end;`   | 使元素浮动到其包含块的结束位置。在 LTR（左至右）语言中，这通常是右边；在 RTL（右至左）语言中，这通常是左边。 |
| `float-right` | `float: right;`        | 使元素浮动到其包含块的右边。                                 |
| `float-left`  | `float: left;`         | 使元素浮动到其包含块的左边。                                 |
| `float-none`  | `float: none;`         | 防止元素浮动，使其不脱离正常文档流。                         |

## 实例

<!-- 创建浮动的图片 -->  
<div class\="float-right ml-6"\>  
    <div class\="relative aspect-w-4 aspect-h-5 sm:aspect-w-16 sm:aspect-h-9 w-20 sm:w-44"\>  
    <img class\="object-cover rounded-lg" src\="https://static.jyshare.com/images/demo/demo2.jpg"\>  
    <div class\="absolute inset-0 ring-1 ring-inset ring-black/10 rounded-lg"\></div\>  
    </div\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout7)

### 清除浮动

Tailwind CSS 中用于控制元素清除浮动的工具类及其对应的 CSS 属性：

| 类名          | CSS 属性及值           | 描述                                                         |
| ------------- | ---------------------- | ------------------------------------------------------------ |
| `clear-start` | `clear: inline-start;` | 清除元素在其起始方向上的浮动元素。在 LTR（左至右）语言中，这通常是左边；在 RTL（右至左）语言中，这通常是右边。 |
| `clear-end`   | `clear: inline-end;`   | 清除元素在其结束方向上的浮动元素。在 LTR（左至右）语言中，这通常是右边；在 RTL（右至左）语言中，这通常是左边。 |
| `clear-left`  | `clear: left;`         | 清除元素左侧的浮动元素。                                     |
| `clear-right` | `clear: right;`        | 清除元素右侧的浮动元素。                                     |
| `clear-both`  | `clear: both;`         | 清除元素两侧的浮动元素。                                     |
| `clear-none`  | `clear: none;`         | 不清除任何浮动元素，允许元素后面跟随浮动元素。               |

## 实例

<article\>  
  <img class\="float-left ..." src\="path/to/image.jpg"\>  
  <img class\="float-right ..." src\="path/to/image.jpg"\>  
  <p class\="clear-left ..."\>测试文本内容...</p\>  
</article\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout8)

### isolate

以下是用于控制堆叠上下文的工具类

| Tailwind 类名    | CSS 属性及值          | 描述                                                         |
| ---------------- | --------------------- | ------------------------------------------------------------ |
| `isolate`        | `isolation: isolate;` | 该元素将创建一个新的堆叠上下文，这意味着它的后代元素不会与外部元素重叠，即使它们有更高的 `z-index` 值。 |
| `isolation-auto` | `isolation: auto;`    | 该元素的堆叠上下文将由用户代理决定，通常与没有设置 `isolation` 属性相同，后代元素可能会与外部元素重叠。 |

这些工具类允许开发者控制元素的堆叠上下文行为，从而影响元素及其后代如何参与堆叠排序。

isolate 类有助于创建一个隔离的环境，其中元素的堆叠顺序不受外部元素影响，而 isolation-auto 则允许浏览器根据默认规则处理堆叠上下文。

使用 isolate 和 isolation-auto 工具类来控制一个元素是否应该显式创建一个新的堆叠上下文。

## 实例

<div class\="isolate ..."\>  
  <!-- ... -->  
</div\>  

‌

### object-fit

以下是用于控制替换元素内容如何缩放的工具类及其对应的 CSS 属性：

| 类名                | CSS 属性及值              | 描述                                                         |
| ------------------- | ------------------------- | ------------------------------------------------------------ |
| `object-contain`    | `object-fit: contain;`    | 保持元素的纵横比，调整大小以完全适应容器，可能会在容器内留有空白。 |
| `object-cover`      | `object-fit: cover;`      | 保持元素的纵横比，调整大小以完全覆盖容器，可能会裁剪掉元素的某些部分。 |
| `object-fill`       | `object-fit: fill;`       | 忽略元素的纵横比，拉伸或压缩以完全填充容器。                 |
| `object-none`       | `object-fit: none;`       | 保持元素的原始尺寸，不进行缩放。                             |
| `object-scale-down` | `object-fit: scale-down;` | 保持元素的纵横比，与 `contain` 类似，但会选取较小的尺寸以适应容器，不会留有空白。 |

使用 object-cover 调整元素内容的大小以覆盖其容器:

## 实例

<div class\="bg-indigo-300 ..."\>  
  <img class\="object-cover h-48 w-96 ..."\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_layout9)