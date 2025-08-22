---
theme: default
---

# 常用的 HTML 组件

<v-switch v-motion :enter="{ y: 20 }">
  <template #0>

## 1. 标题

```html
<h1>这是一级标题</h1>
<h2>这是二级标题</h2>
<h3>这是三级标题</h3>
<h4>这是四级标题</h4>
<h5>这是五级标题</h5>
<h6>这是六级标题</h6>
```

<h1>这是一级标题</h1>
<h2>这是二级标题</h2>
<h3>这是三级标题</h3>
<h4>这是四级标题</h4>
<h5>这是五级标题</h5>
<h6>这是六级标题</h6>

<p style="color: red;">注意：如果你需要使用放大且加粗的文本，请调节它的 CSS 而非直接使用标题来表示加粗加大的文本</p>

  </template>
  <template #1>

## 2. 段落

```html
<p>这是一个段落。</p>
```

  </template>
  <template #2>

## 3. 超链接

我们查看网页的时候也会点击按钮来跳转到其他的页面，而这样的功能就是通过超链接来实现的。

```html
<a href="https://www.example.com">这是一个超链接</a>
```

https://csbigcaptain.github.io/

  </template>
  <template #3>

## 4. 图片

```html
<img src="https://cn.sli.dev/logo.svg" />
```

<img src="https://cn.sli.dev/logo.svg" />

  </template>
  <template #4-6>

## 各标签的简单规律

观察这些标签的代码，你能发现这些标签之间有什么规律吗？

<p style="color: red;"> 提示：可以通过对比这些标签的成对情况观察规律。</p>

```html
<h1> 一级标题 </h1>
<p> 段落 </p>
<a> 超链接 </a>
<img />
```

<div v-click="5">

- 成对的 HTML 标签中间往往会可以填写一些内容（我们称之为插槽）
- 没有插槽的（中间不需要填写内容的）标签一般是单独一个的，我们称它为自闭合标签
- HTML 元素的开始标签和结束标签不一样，结束标签前面有一个 `/`，而自闭合标签的 `/` 写在里面

</div>

  </template>
</v-switch>

---
layout: center
---

<v-switch>
<template #0>

## 煮啵，HTML 前面的部分我记不住怎么办？

</template>
<template #1>

在空白的 HTML 文件中输入一个 `!` 并选中第一个即可快速生成一个简单 HTML 模板！

PS：看来程序员也有我们这样的烦恼......

<img src="/img/html-init.png" />

</template>
</v-switch>

---
transition: slide-up
---
<v-switch>
<template #0>

这里提供了一个参考（`<ol></ol>` 标签表示带数字的列表）：

```html {monaco}
<h1>个人简介</h1>
  
<h2>基本信息</h2>
<p>姓名：张三</p>
<p>年龄：20岁</p>
<p>专业：食品科学与工程</p>
<p>学校：山东理工大学</p>
 
<h2>个人简介</h2>
<p>大家好，我是张三，是一名食品科学与工程专业的学生。我对编程和技术有着浓厚的兴趣，正在学习前端开发技术。</p>

<h2>兴趣爱好</h2>
<p>我喜欢编程、阅读技术书籍、打游戏和听音乐。在业余时间，我也会搞一些项目。</p>
  
<h2>技能</h2>
<ol>
  <li>前端开发，对 Nuxt 框架有一定的理解</li>
  <li>Python</li>
</ol>

<h2>联系方式</h2>
<ul>
  <li>邮箱: <a href="mailto:csbigcaptain@qq.com">csbigcaptain@qq.com</a></li>
  <li>GitHub: <a href="https://github.com/csbigcaptain">https://github.com/csbigcaptain</a></li>
</ul>
```

</template>
<template #1>

## 代码获取

可以去 https://csbigcaptain.github.io/youth-2025shixi/26 中复制代码。

可以在网页中进行简单的编辑，刷新网页即可重置。

</template>
</v-switch>



