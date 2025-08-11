---
layout: center
---

# CSS 简单知识

CSS 决定网页中元素的样式

---
layout: center
---

# 盒模型

最 Minecraft 的一集

---

每个 HTML 元素都是一个盒子（就像 Minecraft 世界的方块一样）

但是每个“盒子”都有它的外边距与内边距就像鸡蛋的蛋壳和蛋清一样：

<img src="/img/css-box-model1.png" width=400 />

---
layout: center
---

# ID 和 Class

---

## 为什么需要 ID 和类？

<v-switch>
<template #0>

我们摘取前面的部分代码。假如我希望增加标题“个人简介”的字号，我们可以用 CSS `h1 { font-size: 30px; }` 来实现，这条 CSS 规则的含义是：令所有的 `h1` 元素的字号为 30 像素，你可以在左下方的代码块中看到我们的修改。

但是这样的规则有一个弊端——它会影响所有的 `h1` 元素，但是我并不希望此发生。因此我们可以为此 `h1` 元素添加一个 ID。然后修改一下我们的规则: `#profile { font-size: 30px; }`，就像右下方的代码块一样。

```html {monaco-diff}
<h1>个人简介</h1>

<h2>基本信息</h2>
<p>姓名：张三</p>
<p>年龄：20岁</p>
<p>专业：食品科学与工程</p>
<p>学校：山东理工大学</p>

<style>
h1 {
  font-size: 30px;
}
</style>
~~~
<h1 id="profile">个人简介</h1>

<h2>基本信息</h2>
<p>姓名：张三</p>
<p>年龄：20岁</p>
<p>专业：食品科学与工程</p>
<p>学校：山东理工大学</p>

<style>
#profile {
  font-size: 30px;
}
</style>
```

</template>
<template #1>

我们继续使用这部分代码，那么现在我希望把基本信息中文字变成黄色（真是奇怪的需求🤔），你可能会改成左边这样的代码。

但是 ID 是不允许重名的，因此这里我们应该使用 Class。

```html {monaco-diff}
<h1 id="profile">个人简介</h1>

<h2>基本信息</h2>
<p id="yellow">姓名：张三</p>
<p id="yellow">年龄：20岁</p>
<p id="yellow">专业：食品科学与工程</p>
<p id="yellow">学校：山东理工大学</p>

<style>
#profile {
  font-size: 30px;
}
#yellow {
  color: yellow;
}
</style>
~~~
<h1 id="profile">个人简介</h1>

<h2>基本信息</h2>
<p class="yellow">姓名：张三</p>
<p class="yellow">年龄：20岁</p>
<p class="yellow">专业：食品科学与工程</p>
<p class="yellow">学校：山东理工大学</p>

<style>
#profile {
  font-size: 30px;
}
.yellow {
  color: yellow;
}
</style>
```
</template>
</v-switch>

---
layout: center
---
## 常用 CSS 属性

---

### `<div>` 与 `<span>` 元素

怎么简单地理解这两个元素呢？

- `<div>` : PPT 里面的文本框，用来包裹 HTML 元素的。
- `<span>` : 一般用来包裹文字用。

```html
<div class="card">
  <h1> 卡片标题 </h1>
  <p> 卡片内容<span class="special-text">它们不会显示出来，猜猜看为什么？</span> </p>
</div>
<style>
.card {
  border: 1px solid #eee;
  border-radius: 5px;
  padding: 10px;
  margin: 10px 0;
}
.special-text {
  display: none;
}
</style>
```

---

### 文字样式相关

- `color` : 文字颜色
  - 颜色名称（如 `red`）
  - 十六进制颜色（如 `#ff0000`）
  -  RGB 颜色、RGBA 颜色以及 HSL 等等 
- `font-size` : 字体大小
  - 最常用的单位是用像素作单位表示的字体大小，如 `16px`
- `font-weight` : 字体粗细
  - `normal`（正常）、`bold`（粗体）、`light`（细字体）、`bolder`（更粗）、`lighter`（更细）
  - 直接使用数字指定粗细，`400` 表示正常字体
- `font-style` : 字体样式（斜体、正常等）
- `text-decoration` : 文字装饰（下划线、删除线等）

注意：VSCode 拥有类型提示，输入几个字母随后用鼠标或者上下方向 + Tab 键可以快速补全关键字。

---

### HTML 元素特性相关

- `width` 和 `height` : 元素的宽度和高度
  - 像素
  - 相对于其父元素的百分比
- `margin` 和 `padding` : 外边距和内边距
  - `margin: 0 auto;` 我们常用这样的设置来使元素水平居中
- `border` : 边框样式
  - `border: 1px solid red;` 表示一个 1 像素宽的实线红色边框
- `background`: 设置背景
  - 可以指定一个颜色，也可以用图片（这里暂且不讲）

`margin` 和 `padding` 可以接收 1 至 4 个参数：

- 一个参数和四个参数：略
- 两个参数：第一个指上下的参数，第二个指左右的参数
- 三个参数（了解）：第一个指上边距参数，第二个指左右边距参数，最后一个指下边距参数
