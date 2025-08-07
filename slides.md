---
theme: default
title: 青春在线 2025 暑假实习生培训
background: /img/maple.webp
author: Youthol
transition: slide-left
---

# 青春在线 2025 暑假实习生培训

程序部

<div class="absolute bottom-10">
  <span class="font-700">
    2025-8-15
  </span>
</div>

<div class="absolute bottom-10 right-12 w-50">
  <img src="https://youth.sdut.edu.cn/_upload/tpl/05/c2/1474/template1474/images/logo.png" />
</div>

---
layout: default
transition: slide-up
---

# 主要内容

- 程序部简介
- 扫盲课
- 软件下载
- HTML 和 CSS 相关
- 实操网页
- 答疑环节

---
layout: center
---

# 程序部简介

---
layout: iframe-right
url: https://youthol.github.io/YoutholTrainingDocs/
transition: slide-up
---

我们是青春在线最“神秘”的部门，为青春在线网站的一些活动提供技术支持，以及网站的维护工作等。

部门技术交流氛围浓厚，也有来自各个专业的同学，欢迎有志于技术提升的小伙伴加入我们！

右边是我们的其中一个项目，是我们为部门新生培训准备的在线文档。

网页链接：https://youthol.github.io/YoutholTrainingDocs/

项目链接：https://github.com/youthol/YoutholTrainingDocs

---
layout: center
---

# 扫盲课环节

---
layout: center
---

<v-switch>
  <template #0>
    <h1 class="font-bold">为什么要进行扫盲课？</h1>
  </template>
  <template #1>
    <img src="/img/smk-example.png" />
  </template>
</v-switch>

---
layout: center
---

# 为什么要用压缩包？

- **需要发送的文件众多**：完整的游戏里面包含了大量的动态链接库以及游戏模型文件，用户根本无法从网盘中逐个下载，如果把它们整合成一个文件就方便的多
- **平台限制**：大多数平台无法支持传输文件夹（例如 QQ 微信等）
- **优化文件的体积**：将文件压缩可以减小文件总体积，部分游戏压缩以后能节约 40%~50% 的空间

<!--
寻找几个游戏的资源文件展示里面文件结构
-->

---
layout: center
---

# 常用的压缩软件推荐：

- 7-Zip：使用率相当高的免费开源压缩软件，安装包仅仅只有 1.6M！还支持文件校验功能
- Bandizip：相对于前者提供了一些更加实用的功能，，个人感觉综合体验最好。但是免费版有广告，不过网上有无广告版本
- WinRAR：个人免费版有广告，独占压缩 RAR 文件的功能（专利），值得庆幸的是，网上也有去广告版本

煮啵最推荐的还是 7-zip ，如果能搞到无广告版的话，Bandizip 是最好用的，WinRAR 只在特殊情况才会用。

- 7-zip 官网：https://www.7-zip.org/
- Bandizip 官网：https://www.bandisoft.com/bandizip/

---
layout: default
transition: slide-up
---

<v-click hide at="1">

## 文件路径是什么

文件路径用来表示文件在电脑中的位置，我们往往会用到几种特殊的方法来表示路径，我们这里以一个项目的文件夹为例，下面是这个文件夹的结构：

</v-click>

<div
  v-motion
  :initial="{ y: 0 }"
  :click-1="{ y: -110, transition: { delay: 100 } }"
>

```
Project
├── demo1
│   ├── js
│   └── index.html
├── demo2
│   ├── css
│   ├── font
│   ├── img
│   │   └── logo.jpg
│   ├── js
│   └── index.html
└── index.html

```

</div>

<v-click hide at="1">

在这个文件树中，不带后缀是文件夹，带后缀的则是文件，例如最顶层的 `Project` 是一个文件夹，里面有三个文件夹 `demo1`、`demo2`、`demo3` 以及一个文件 `index.html`。

</v-click>

<v-switch
  v-motion
  :initial="{ y: 0 }"
  :click-1="{ y: -160 }"
>
<template #2>

相对路径与绝对路径：

- 绝对路径：是相对于根目录下的路径，例如 `c:/Windows/System32/cmd.exe`
- 相对路径：是相对于某一文件的路径

假如你想在 `/index.html` 中链接 `/demo1/index.html` 文件的话，可以用 `./demo1/index.html` 来表示。反过来的话，如果你想在 `/demo1/index.html` 中链接 `/index.html` 文件的话，可以用 `../index.html` 来表示。

</template>
<template #3>

我们也会用一种特殊的绝对路径格式，它省略了前面项目文件夹所在的位置，例如 `/demo1/index.html`，它表示的是从根目录开始的路径，也就是 `Project` 文件夹的位置。

我们在部署网页的时候只会把这个 `Project` 文件夹放到服务器上，我们并不关心 `Project` 文件夹的位置。

</template>
<template #4>

<img src="/img/lujing-example.png" width="1200" />

相反，如果我们在代码中包含了 `Project` 文件夹的位置，反而会降低代码的可移植性。因为代码拷贝到其他的设备的时候并无法保证能放到同样的位置，详见上图。

</template>
</v-switch>

<!--
让观众猜测一下下面相对路径的含义
-->

---
layout: center
---

# 软件下载

---
transition: slide-up
---

## 怎么避免下载到不正规的软件？

<v-switch v-motion :initial="{ y: 20 }">
<template #0-2>

### 1. 尽量选择软件官网或者是正规的下载站

</template>
<template #1>

<img src="/img/xiazai-guanwang.png" width="800" />

</template>
<template #2-4>

### 2. 在野下载站中下载软件注意安全

</template>
<template #3>

<img src="/img/xiazai-xiazaizhan.png" width="800" />

</template>
<template #4-6>

### 3. 检查下载的文件

</template>
<template #5>

**一般**下载的安装包文件名以及安装包的图标是与软件名字相关的，而且**一般**不会使用中文名字

</template>
<template #6-8>

### 4. 在安装过程中遇到微信支付宝扫码支付之后才能使用的情况均为诈骗！

</template>
<template #7>

真正的付费软件一般安装完成之后才会检查你的授权情况，而且往往会提供试用期，在安装过程中收费特别是要求扫码支付才能用的现象肯定是诈骗！

</template>
</v-switch>


<!--
1. 下载站下载注意不要误下载电脑管家
2. 不要选择高速下载
-->

---

# Visual Studio Code 下载以及安装

<v-switch v-motion :initial="{ y: 20 }">
<template #0-1>

官网：https://code.visualstudio.com/

进入网站点击中间的 Download 按钮即可下载，下载完成后打开，按照默认设置安装（无脑下一步）即可。

如果官网无法访问可以在腾讯应用中心下载：https://pc.qq.com/detail/16/detail_22856.html

【😍推荐】或者是从微软应用商店一键安装完成：https://apps.microsoft.com/detail/xp9khm4bk9fz7q

</template>
</v-switch>

---

# VS Code 插件安装

VS Code 默认语言为英文，需要安装汉化插件，另外在学习过程中需要实时查看网页效果，也需要相关插件

<v-switch v-motion :initial="{ y: 10 }">

<template #0-1>

打开 VS Code，点击左侧的扩展按钮：

<img src="/img/code-kuozhan.png" width="630" />

</template>
<template #1-2>

安装中文扩展：

<img src="/img/code-chajian1.png" width="630" />

</template>

<template #2-3>

安装预览插件：

<img src="/img/code-chajian2.png" width="630" />

</template>
</v-switch>

---

# 新建网页项目

<v-switch v-motion :initial="{ y: 10 }">
<template #0-1>

## 1. 新建文件夹

找一个自己喜欢的位置，新建一个文件夹，并起一个名字（例如`web-project`）

<img src="/img/xiangmu-xinjian-wjj.png" width="600" />

</template>
<template #1-2>

## 2. 在 VS Code 中打开文件夹

打开 VS Code，点击左上角的文件（英文版是 File ）按钮，选择“打开文件夹”（Open Folder...），然后选择刚才新建的文件夹。

或者是按下快捷键 `Ctrl + Shift + N`（或者是点击左上角文件按钮并选择新建窗口），然后把你新建的文件夹用鼠标拖入新窗口中，然后关闭掉旧的窗口就可以了。

</template>
<template #2-3>

## 3. 初始化项目

在 VS Code 中打开的文件夹中，右键点击空白处，选择“新建文件”（New File...），创建一个名为 `index.html` 的文件。

<img src="/img/xiangmu-xinjian-wj.png" width="600" />

</template>
<template #3-4>

非常好！以此类推，你需要再新建一个名为 `css` 的文件夹。并根据自己的需要，再新建 `js` `img` `media` 等文件夹。

- `css` 文件夹用来储存我们的 CSS 文件
- `js` 文件夹用来储存我们的 JavaScript 文件（本次培训我们不会用到 JavaScript）
- `img` 文件夹用来储存我们需要的图片
- `media` 文件夹用来储存我们需要的音视频文件

本次培训我们只需要创建 `css` 文件夹即可，其他的文件夹大家在完成作业的时候可能会用到。

大功告成！现在我们项目的文件结构应该是这个样子的：

```
Project
├── css
├── img
├── js
├── media
└── index.html
```

</template>
</v-switch>




