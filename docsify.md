# 文档站点生成器--docsify
>> [docsify](#welcome) 一个文档站点生成器<br>⚡特点是简单轻巧、无须静态构建的 `html` 文件、多个主题，利用 `MarkDown` 文档生成项目站点。

---

<div align="right"><img src="https://github.com/fmw666/my-image-file/blob/master/images/gif/rabit-jump.gif" width="200"></div><br>

&emsp;&emsp;*"我们对于 [docsify](#welcome) 的引入是为了将我们的教程、技术类文档利用 `GitHub Pages`，做成网站的形式展示给更多的用户。相比于之前的 `MarkDown` 文档展示，利用这个生成器能加强文档的美观度、动画的整体性、游览的流畅度等，其中滚动侧栏的目录、以及全局搜索功能更是能给用户一个非常良好的体。总结于此，所以我们决定采用这个方式。"*

*---*

**[`docsify`](#welcome) 相关网站：**

* 官方网站 [https://docsify.js.org/#/](https://docsify.js.org/#/)

* 官方 [GitHub](https://github.com/docsifyjs/docsify)

*---*

<div align=center><img src="https://github.com/fmw666/my-image-file/blob/master/images/small/give-me-five.png" width="200"></div>

## 简单入门指南

*---*

> <b>注：</b>以下内容全基于作者搭建一个<b>《计算机操作系统》</b>文档网站所用<br><br>
<i>`GitHub` 地址：[https://github.com/fmw666/Operating-System](https://github.com/fmw666/Operating-System/)</i><br>
<i>网站展示地址：[https:](https:)</i><br>
>> 更多关于 [`docsify`](#welcome) 的完整学习，请参考其官网：[https://docsify.js.org/#/quickstart](https://docsify.js.org/#/quickstart)

*---*

1. [全局安装](#全局安装)

1. [初始化](#初始化)

1. [本地运行预览](#本地运行预览)

1. [添加封面](#添加封面)

*---*

### 全局安装

&emsp;&emsp;💡 全局安装有助于在本地初始化和预览网站。

  ```shell
  npm i docsify-cli -g
  ```

<div align=right><a href="#简单入门指南">⬆ return to top</a></div>

### 初始化

&emsp;&emsp;📂 在空文件夹下启动 shell 用以创建我们的项目。

  ```bash
  docsify init ./docs
  ```
  
🛠 命令执行后会在文件夹下出现我们 `docs` 文件夹，其中 `./docs` 下：

+ [`index.html`](#welcome) 作为入口文件

+ [`README.md`](#welcome) 作为主页

+ [`.nojekyll`](#welcome) 防止GitHub页面忽略以下划线开头的文件

<div align=right><a href="#简单入门指南">⬆ return to top</a></div>

### 本地运行预览

&emsp;&emsp;💻 在启动后，您可以在浏览器中预览您的网站：http://localhost:3000

  ```bash
  docsify serve docs
  ```
  
<div align=right><a href="#简单入门指南">⬆ return to top</a></div>

### 添加封面

&emsp;&emsp;⚙ 设置 [`coverpage`](#welcome) 为 [true](#welcome)，并创建一个 [`\_coverpage.md`](#welcome)：

```html
<!-- index.html -->

<script>
  window.$docsify = {
    coverpage: true
  }
</script>
<script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
```

```text
<!-- _coverpage.md -->

<img src="_media/icon.png" width="100">

# 计算机操作系统

- 全文基于汤子瀛的《计算机操作系统》第四版--西安电子科技大学出版社

[![stars](https://badgen.net/github/stars/fmw666/Operating-System?icon=github&color=4ab8a1)](https://github.com/fmw666/Operating-System) 
[![forks](https://badgen.net/github/forks/fmw666/Operating-System?icon=github&color=4ab8a1)](https://github.com/fmw666/Operating-System)

[GitHub](https://github.com/fmw666/Operating-System/)
[开始阅读](README.md)
```

> 💡 在 `./docs` 下创建 `_media` 文件夹，用于存放我们的媒体文件

<div align=right><a href="#简单入门指南">⬆ return to top</a></div>

### xxx
