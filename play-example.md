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

接着，我们在 `/css/` 目录下创建 `common.css` 文件，这个文件存储着我提供的模板的样式。

新建完文件后，我们的文件目录应该是这样的：

```

```
