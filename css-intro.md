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

12