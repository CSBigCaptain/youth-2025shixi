---
layout: center
---

# 实操环节

制作个人简介页面

---

## 如何引入 CSS ？

<v-switch v-motion :enter=" { y: 30 } ">
<template #0>

### 1. 在 HTML 中引用 CSS

在 `<head>` 标签中引入 CSS 文件。VSCode 提供了自动补全，在输入框中输入 `link:css` 然后按下回车即可生成此语句。

```html
<head>
  <link rel="stylesheet" href="styles.css" >
</head>

```

</template>
<template #1>

### 2. 在 HTML 中通过 `<style>` 标签中引入

```html
<style>
  /* 在这里编写 CSS 代码 */
  body {
    background-color: lightblue;
  }
</style>
```

`<style>` 标签的位置没有要求，一般我们都写在 `<body>` 标签内。

</template>
<template #2>

### 3. 在 CSS 中引入 CSS

为了便于维护，我们一个页面有时候会有两三个 CSS 文件，我们可以在主 CSS 文件中引入另外几个共用的文件，这样的话我们在 HTML 这边只需要引入一个 CSS 文件即可。

```css
/* index.css */

/* 引入网站头部、内容背景以及页脚样式 */
@import url("./website-header.css");
@import url("./website-content-background.css");
@import url("./website-footer.css");
```

</template>
</v-switch>

---
layout: center
---

## 引入代码

由于课程时间有限，我已提前完成了一部分代码，复制这些代码到编辑器中（代码块右上角有复制按钮）

---

`index.html` 文件

```html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./css/index.css">
    <title>在这里自定义网站显示在浏览器标签页上的题目</title>
</head>
<body>
    <header class="nav">
        <div class="logo">
            Blog
        </div>
        <nav>
            <ul>
                <li><a href="./index.html">首页</a></li>
                <li><a href="./index.html">首页</a></li>
            </ul>
        </nav>
    </header>
    <main>网页的内容在这里完成即可</main>
</body>
</html>
```

---

接着，我们在 `/css/` 目录下创建 `common.css` 以及 `index.css` 文件。

新建完文件后，我们的文件树应该是这样的：

```
Project
├── css
│   ├── common.css
│   └── index.css
├── img (可选)
├── js (可选)
├── media (可选)
└── index.html
```

---

这个是 `common.css` 文件的代码（使用代码块右上角的复制按钮复制）：

```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.nav a,
.nav a:visited,
.nav a:hover,
.nav a:active {
  /* 清除超链接的默认样式 */
  color: white;
  text-decoration: none;
}

.nav ul {
  /* 清除列表前面的小圆点 */
  list-style: none;
}

.nav {
  width: 100%;
  background-color: #37474f;
  overflow: hidden;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
}

.nav .logo {
  color: white;
  font-size: 24px;
  font-weight: bold;
}

.nav nav {
  height: 100%;
}

.nav ul {
  display: flex;
  align-items: center;
  height: 100%;
}

.nav ul li {
  width: 80px;
  height: 100%;
}

.nav ul li a {
  color: #b0bec5;
  line-height: 60px;
  height: 100%;
  text-align: center;
  display: block;
}

.nav ul li a:hover {
  background-color: #546e7a;
  transition: all 0.35s ease;
}

body {
    background: #78909c;
}

main {
    padding: 50px;
    width: 75%;
    margin: 0 auto;
    background: #455a64;
    min-height: 1000px;
    color: #cfd8dc;
}

```

---
transition: slide-up
---

接下来我们在 `index.css` 文件中引入我们的 `common.css` 文件：

```css
@import url("./common.css");
```

通过这些引用的代码，我们已经完成了网页中绝大多数内容的开发。

