## Tailwind CSS 重用样式

在 Tailwind CSS 中重用样式是一个常见的需求，尤其是当项目规模增长时，你可能会发现在不同的地方需要重复相同的样式组合。

在 Tailwind CSS 中，样式通过低级的工具类（utility classes）进行实现，这种方式非常适合避免过早抽象（premature abstraction）的问题，能够让你灵活控制样式，并且在许多场景下非常高效。

然而，随着项目的增大，代码中不可避免地会出现重复使用相同的工具类组合的情况，这就可能导致冗余和维护上的困难。这个时候，如何管理重复的样式并创建可复用的抽象就显得尤为重要。

### 为什么会有重复样式？

Tailwind CSS 的核心理念是 工具优先（Utility-First）。通过组合一系列低级的工具类，你可以非常精确地控制元素的样式。虽然这种方式在初期很强大，但随着项目越来越复杂，尤其是在处理常见的 UI 元素（如按钮、卡片、头像等）时，往往会在多个地方重复使用相同的工具类。

考虑以下模板，其中每个头像图片都使用了相同的工具类：

## 实例

<div class\="flex space-x-4"\>  
  <img class\="w-16 h-16 rounded-full border-2 border-white" src\="/img/avatar1.jpg" alt\="User 1"\>  
  <img class\="w-16 h-16 rounded-full border-2 border-white" src\="/img/avatar2.jpg" alt\="User 2"\>  
  <img class\="w-16 h-16 rounded-full border-2 border-white" src\="/img/avatar3.jpg" alt\="User 3"\>  
  <img class\="w-16 h-16 rounded-full border-2 border-white" src\="/img/avatar4.jpg" alt\="User 4"\>  
  <img class\="w-16 h-16 rounded-full border-2 border-white" src\="/img/avatar5.jpg" alt\="User 5"\>  
</div\>  

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trytailwindcss_rs1)

这里，每个头像图片都使用了相同的工具类组合：w-16 h-16 rounded-full border-2 border-white。

这种做法虽然简洁，但随着头像的数量增多，代码变得越来越冗长，而且如果需要调整这些样式（如改变边框颜色或圆角大小），则需要手动修改每个类，导致维护困难。

### 解决重复样式的方案

Tailwind通过使用 @apply、@layer 和 variants 等功能，你可以轻松创建可复用的样式，减少代码重复，提高开发效率和可维护性。

+   **`@apply`**：将常用的工具类组合成一个自定义类，减少重复代码。
+   **`@layer`**：定义样式层级，将不同的样式组合组织起来，便于管理。
+   **`variants`**：扩展工具类，使得样式可以根据状态（如响应式、悬停、聚焦等）变化。

**1\. 使用 @apply 指令创建自定义的类**

Tailwind 提供了 @apply 指令，可以在 CSS 文件中将一组常用的工具类组合成一个自定义的类，这样就可以减少 HTML 中的重复代码。通过这种方式，你可以将重复的工具类抽象成一个可复用的类。

```
@tailwind base;
@tailwind components;
@tailwind utilities;

/* 在你的 CSS 文件中 */
.avatar {
  @apply w-16 h-16 rounded-full border-2 border-white;
}
```

然后，在 HTML 中，你只需使用这个自定义的 avatar 类，而不必再重复写相同的工具类：

## 实例

<div class\="flex space-x-4"\>  
  <img class\="avatar" src\="/img/avatar1.jpg" alt\="User 1"\>  
  <img class\="avatar" src\="/img/avatar2.jpg" alt\="User 2"\>  
  <img class\="avatar" src\="/img/avatar3.jpg" alt\="User 3"\>  
  <img class\="avatar" src\="/img/avatar4.jpg" alt\="User 4"\>  
  <img class\="avatar" src\="/img/avatar5.jpg" alt\="User 5"\>  
</div\>  

通过这种方式，你避免了在 HTML 中重复书写相同的工具类，同时也便于未来对样式的维护和修改。

编译 Tailwind CSS 使用 Tailwind CLI 或 PostCSS 进行编译：

```
npx tailwindcss -i ./styles.css -o ./output.css --watch
```

编译后生成的 output.css 文件会将 @apply 替换为具体的 CSS 样式。

**2\. 利用 @layer 和 @apply 定义更复杂的样式**

如果你有一组更复杂的、跨多个元素的工具类组合，可以使用 @layer 来定义这些样式，并通过 @apply 组合它们。

```
@tailwind base;
@tailwind components;
@tailwind utilities;

/* 定义一个自定义的层级，并应用一组工具类 */
@layer components {
  .avatar {
    @apply w-16 h-16 rounded-full border-2 border-white shadow-md;
  }
  .button {
    @apply px-4 py-2 bg-blue-500 text-white rounded-lg;
  }
}
```

然后，在 HTML 中，你依然可以通过 avatar 和 button 类来使用这些预定义的样式。

## 实例

<div class\="flex space-x-4"\>  
  <img class\="avatar" src\="/img/avatar1.jpg" alt\="User 1"\>  
  <button class\="button"\>点击我</button\>  
</div\>  

这种方式允许你在 CSS 文件中定义可复用的类，并且使得 HTML 保持简洁。

**3\. 使用 Tailwind CSS 的 variants 功能**

在 Tailwind CSS 中，variants 允许你通过不同的状态（如响应式、悬停、聚焦等）来扩展已有的工具类。如果你的项目中某些工具类组合需要根据不同的状态或设备尺寸来变化，可以通过 variants 来创建具有响应式和交互状态的复用样式。

例如，创建一个响应式头像样式：

```
@layer components {
  .avatar {
    @apply w-16 h-16 rounded-full border-2 border-white;
  }

  /* 响应式变化：在较大的屏幕上使用更大的头像 */
  @media (min-width: 768px) {
    .avatar {
      @apply w-24 h-24;
    }
  }
}
```

这种方式确保了头像在不同的设备上保持一致的外观，并且能够根据屏幕尺寸自动调整大小。