## Bootstrap4 小工具

Bootstrap4 提供了一些小工具，可以让我们不用写 CSS 代码就能实现想要的效果。

* * *

## 边框

使用 border 类可以添加或移除边框:

## 实例

<span class\="border"\></span\> <span class\="border border-0"\></span\> <span class\="border border-top-0"\></span\> <span class\="border border-right-0"\></span\> <span class\="border border-bottom-0"\></span\> <span class\="border border-left-0"\></span\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_util_borders)

* * *

## 边框颜色

Bootstrap4 提供了一些类来设置边框颜色:

## 实例

<span class\="border border-primary"\></span\> <span class\="border border-secondary"\></span\> <span class\="border border-success"\></span\> <span class\="border border-danger"\></span\> <span class\="border border-warning"\></span\> <span class\="border border-info"\></span\> <span class\="border border-light"\></span\> <span class\="border border-dark"\></span\> <span class\="border border-white"\></span\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_util_borders_colors)

* * *

## 边框圆角设置

使用rounded 类可以添加圆角边框:

## 实例

<span class\="rounded"\></span\> <span class\="rounded-top"\></span\> <span class\="rounded-right"\></span\> <span class\="rounded-bottom"\></span\> <span class\="rounded-left"\></span\> <span class\="rounded-circle"\></span\> <span class\="rounded-0"\></span\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_util_borders_rounded)

* * *

## 浮动

.float-right 类用于设置元素右浮动， .float-left 设置元素左浮动, .clearfix 类用于清除浮动:

## 实例

<div class\="clearfix"\> <span class\="float-left"\>左浮动</span\> <span class\="float-right"\>右浮动</span\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_util_float)

* * *

## 响应式浮动

我们看可以设置浮动 (.float-\*-left|right - \* 为 sm, md, lg 或 xl)的方向依赖于屏幕的大小:

## 实例

<div class\="float-sm-right"\>在大于小屏幕尺寸上右浮动</div\><br\> <div class\="float-md-right"\>在大于中等屏幕尺寸上右浮动</div\><br\> <div class\="float-lg-right"\>在大于大屏幕尺寸上右浮动</div\><br\> <div class\="float-xl-right"\>在大于超大屏幕尺寸上右浮动</div\><br\> <div class\="float-none"\>没有浮动</div\>

[尝试一下 »](https://www.runoob.com/try/try2.php?filename=trybs4_util_float_resp)

* * *

## 居中对齐

使用 .mx-auto 类来设置居中对齐:

## 实例

<div class\="mx-auto bg-warning" style\="width:150px"\>居中显示</div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_util_center)

* * *

## 宽度

元素上使用 w-\* 类 (.w-25, .w-50, .w-75, .w-100, .mw-100) 来设置宽度:

## 实例

<div class\="w-25 bg-warning"\>宽度 25%</div\> <div class\="w-50 bg-warning"\>宽度 50%</div\> <div class\="w-75 bg-warning"\>宽度 75%</div\> <div class\="w-100 bg-warning"\>宽度 100%</div\> <div class\="mw-100 bg-warning"\>最大宽度 100%</div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_util_width)

* * *

## 高度

元素上使用 h-\* 类 (.h-25, .h-50, .h-75, .h-100, .mh-100) 来设置高度:

## 实例

<div style\="height:200px;background-color:#ddd"\> <div class\="h-25 bg-warning"\>高度 25%</div\> <div class\="h-50 bg-warning"\>高度 50%</div\> <div class\="h-75 bg-warning"\>高度 75%</div\> <div class\="h-100 bg-warning"\>高度 100%</div\> <div class\="mh-100 bg-warning" style\="height:500px"\>最大高度 100%</div\> </div\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_util_height)

* * *

## 间距

间距设置语法如下:

```
{property}{sides}-{size}  // 适用 xs(<=576px)
{property}{sides}-{breakpoint}-{size} // 适用 sm (>=576px), md (>=768px), lg (>=992px), xl (>=1200px) 
```

> breakpoints 指的是屏幕宽度: xs (<=576px), sm (>=576px), md (>=768px), lg (>=992px), xl (>=1200px)。

property 代表属性，包含：

+   `m` - 用来设置 `margin`
+   `p` - 用来设置 `padding`

sides 主要指方向：

+   `t` - 用来设置 `margin-top` 或 `padding-top`
+   `b` - 用来设置 `margin-bottom` 或 `padding-bottom`
+   `l` - 用来设置 `margin-left` 或 `padding-left`
+   `r` - 用来设置 `margin-right` 或 `padding-right`
+   `x` - 用来设置 `*-left` 和 `*-right`
+   `y` - 用来设置 `*-top` 和 `*-bottom`
+   blank - 用来设置元素在四个方向的 `margin` 或 `padding`

size 指的是边距的大小：

+   `0` - 设置 `margin` 或 `padding` 为 `0`
+   `1` - 设置 `margin` 或 `padding` 为 `$spacer * .25`
+   `2` - 设置 `margin` 或 `padding` 为 `$spacer * .5`
+   `3` - 设置 `margin` 或 `padding` 为 `$spacer`
+   `4` - 设置`margin` 或 `padding` 为 `$spacer * 1.5`
+   `5` - 设置 `margin` 或 `padding` 为 `$spacer * 3`
+   `auto` - 设置 `margin` 为 auto

外边距 **margin** 可以设置负数，在数字前面添加字母 **"n"** :

+   `n1` - 设置 margin 为 -.25rem (如果 font-size 为 16px 则为 -4px )
+   `n2` - 设置 margin 为 -.5rem (如果 font-size 为 16px 则为 -8px)
+   `n3` - 设置 margin 为 -1rem (如果 font-size 为 16px 则为 -16px)
+   `n4` - 设置 margin 为 -1.5rem (如果 font-size 为 16px 则为 -24px)
+   `n5` - 设置 margin 为 -3rem (如果 font-size 为 16px 则为 -48px)

看下部分边距的源码设置：

```
.mt-0 {
  margin-top: 0 !important;
}

.ml-1 {
  margin-left: ($spacer * .25) !important;
}

.px-2 {
  padding-left: ($spacer * .5) !important;
  padding-right: ($spacer * .5) !important;
}

.p-3 {
  padding: $spacer !important;
}
```

## 实例

<div class\="mx-auto" style\="width: 200px;"\> 元素设置居中 </div\> <form \> <div class\="form-row"\> <div class\="form-group"\> <label for\="text" class\="mt-2"\>设置 margin-top：</label\> <input type\="text" class\="form-control" id\="text" placeholder\="email"\> <label for\="color" class\="mt-2"\>颜色：</label\> <input type\="color" id\="color" class\="form-control" style\="width: 60px;padding: 4px;" autocomplete\="off" value\="#656565"\> </div\> </div\> </form\>

[尝试一下 »](https://www.runoob.com/try/try.php?filename=trybs4_utilities13)

### 更多实例

<table class="reference"><tbody><tr><td><code>.m-# / m-*-#</code></td><td>设置所有边的外边距</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_spacing" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.mt-# / mt-*-#</code></td><td>margin top</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_mt-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.mb-# / mb-*-#</code></td><td>margin bottom</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_mb-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.ml-# / ml-*-#</code></td><td>margin left</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_ml-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.mr-# / mr-*-#</code></td><td>margin right</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_mr-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.mx-# / mx-*-#</code></td><td>margin left 与 right</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_mx-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.my-# / my-*-#</code></td><td>margin top 与 bottom</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_my-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.p-# / p-*-#</code></td><td>使用边设置 padding</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_p-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.pt-# / pt-*-#</code></td><td>padding top</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_pt-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.pb-# / pb-*-#</code></td><td>padding bottom</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_pb-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.pl-# / pl-*-#</code></td><td>padding left</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_pl-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.pr-# / pr-*-#</code></td><td>padding right</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_pr-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.py-# / py-*-#</code></td><td>padding top 与 bottom</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_py-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr><tr><td><code>.px-# / px-*-#</code></td><td>padding left 与 right</td><td><a href="https://www.runoob.com/try/try.php?filename=trybs4_util_px-responsive" class="tryitbtn" target="_blank" rel="noopener">尝试一下</a></td></tr></tbody></table>