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

1. [完善目录主页](#完善目录主页)

1. [添加条目内容](#添加条目内容)

1. [完善 index.html](#完善%20index.html)

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

&emsp;&emsp;⚙ 设置 [`coverpage`](#welcome) 为 [true](#welcome)，并创建一个 [`_coverpage.md`](#welcome)：

  ```html
  <!-- index.html -->

  <script>
    window.$docsify = {
      coverpage: true
    }
  </script>
  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
  ```

  ```markdown
  <!-- _coverpage.md -->

  <img src="\_media/icon.png" width="100">

  # 计算机操作系统

  - 全文基于汤子瀛的《计算机操作系统》第四版--西安电子科技大学出版社

  [![stars](https://badgen.net/github/stars/fmw666/Operating-System?icon=github&color=4ab8a1)](https://github.com/fmw666/Operating-System) 
  [![forks](https://badgen.net/github/forks/fmw666/Operating-System?icon=github&color=4ab8a1)](https://github.com/fmw666/Operating-System)

  [GitHub](https://github.com/fmw666/Operating-System/)
  [开始阅读](README.md)
  ```

> 💡 在 `./docs` 下创建 `_media` 文件夹，用于存放我们的媒体文件

<div align=right><a href="#简单入门指南">⬆ return to top</a></div>

### 完善目录主页

  ```markdown
  <!-- README.md -->

  - [《操作系统》目录](#)

  ## 第一章 操作系统引论

  - [1.1 操作系统的目标和作用](notes/1.1%20操作系统的目标和作用.md) </br>
  - [1.2 操作系统的发展过程](notes/1.2%20操作系统的发展过程.md) </br>
  - [1.3 操作系统的基本特性](notes/1.3%20操作系统的基本特性.md) </br>
  - [1.4 操作系统的主要功能](notes/1.4%20操作系统的主要功能.md)</br>
  - [1.5 操作系统的结构设计](notes/1.5%20操作系统的结构设计.md)</br>
  - [习题](notes/1.习题.md)

  ## 第二章 进程的描述与控制

  - [2.1 前趋图和程序执行](notes/2.1%20前趋图和程序执行.md) </br>
  - [2.2 进程的描述](notes/2.2%20进程的描述.md) </br>
  - [2.3 进程控制](notes/2.3%20进程控制.md) </br>
  - [2.4 进程同步](notes/2.4%20进程同步.md)</br>
  - [2.5 经典进程的同步问题](notes/2.5%20经典进程的同步问题.md)</br>
  - [2.6 进程通信](notes/2.6%20进程通信.md) </br>
  - [2.7 线程（Threads）的基本概念](notes/2.7%20线程（Threads）的基本概念.md)</br>
  - [2.8 线程的实现](notes/2.8%20线程的实现.md)</br>
  - [习题](notes/2.习题.md)

  ## 第三章 处理机调度与死锁

  - [3.1 处理机调度的层次和调度算法的目标](notes/3.1%20处理机调度的层次和调度算法的目标.md) </br>
  - [3.2 作业与作业调度](notes/3.2%20作业与作业调度.md) </br>
  - [3.3 进程调度](notes/3.3%20进程调度.md) </br>
  - [3.4 实时调度](notes/3.4%20实时调度.md)</br>
  - [3.5 死锁概述](notes/3.5%20死锁概述.md)</br>
  - [3.6 预防死锁](notes/3.6%20预防死锁.md) </br>
  - [3.7 避免死锁](notes/3.7%20避免死锁.md)</br>
  - [3.8 死锁的检测与解除](notes/3.8%20死锁的检测与解除.md)</br>
  - [习题](notes/3.习题.md)

  ## 第四章 存储器管理

  - [4.1 存储器的层次结构](notes/4.1%20存储器的层次结构.md) </br>
  - [4.2 程序的装入和链接](notes/4.2%20程序的装入和链接.md) </br>
  - [4.3 连续分配存储管理方式](notes/4.3%20连续分配存储管理方式.md) </br>
  - [4.4 对换（Swapping）](notes/4.4%20对换（Swapping）.md)</br>
  - [4.5 分页存储管理方式](notes/4.5%20分页存储管理方式.md)</br>
  - [4.6 分段存储管理方式](notes/4.6%20分段存储管理方式.md) </br>
  - [习题](notes/4.习题.md)

  ## 第五章 虚拟存储器

  - [5.1 虚拟存储去概述](notes/5.1%20虚拟存储去概述.md) </br>
  - [5.2 请求分页存储管理方式](notes/5.2%20请求分页存储管理方式.md) </br>
  - [5.3 页面置换算法](notes/5.3%20页面置换算法.md) </br>
  - [5.4 “抖动”与工作集](notes/5.4%20“抖动”与工作集.md)</br>
  - [5.5 请求分段存储管理方式](notes/5.5%20请求分段存储管理方式.md)</br>
  - [习题](notes/5.习题.md)

  ## 第六章 输入输出系统

  - [6.1 I/O 系统的功能、模型和接口](notes/6.1%20I/O%20系统的功能、模型和接口.md) </br>
  - [6.2 I/O 设备和设备控制器](notes/6.2%20I/O%20设备和设备控制器.md) </br>
  - [6.3 中断机构和中断处理程序](notes/6.3%20中断机构和中断处理程序.md) </br>
  - [6.4 设备驱动程序](notes/6.4%20设备驱动程序.md)</br>
  - [6.5 与设备无关的 I/O 软件](notes/6.5%20与设备无关的%20I/O%20软件.md)</br>
  - [6.6 用户层的 I/O 软件](notes/6.6%20用户层的%20I/O%20软件.md) </br>
  - [6.7 缓冲区管理](notes/6.7%20缓冲区管理.md)</br>
  - [6.8 磁盘存储器的性能和调度](notes/6.8%20磁盘存储器的性能和调度.md)</br>
  - [习题](notes/6.习题.md)

  ## 第七章 文件管理

  - [7.1 文件和文件系统](notes/7.1%20文件和文件系统.md) </br>
  - [7.2 文件的逻辑结构](notes/7.2%20文件的逻辑结构.md) </br>
  - [7.3 文件目录](notes/7.3%20文件目录.md) </br>
  - [7.4 文件共享](notes/7.4%20文件共享.md)</br>
  - [7.5 文件保护](notes/7.5%20文件保护.md)</br>
  - [习题](notes/7.习题.md)

  ## 第八章 磁盘存储器的管理

  - [8.1 外存的组织方式](notes/8.1%20外存的组织方式.md) </br>
  - [8.2 文件存储空间的管理](notes/8.2%20文件存储空间的管理.md) </br>
  - [8.3 提高磁盘 I/O 速度的途径](notes/8.3%20提高磁盘%20I/O%20速度的途径.md) </br>
  - [8.4 提高磁盘可靠性的技术](notes/8.4%20提高磁盘可靠性的技术.md)</br>
  - [8.5 数据一致性控制](notes/8.5%20数据一致性控制.md)</br>
  - [习题](notes/8.习题.md)
  ```

<div align=right><a href="#简单入门指南">⬆ return to top</a></div>

### 添加条目内容

&emsp;&emsp;📁 新建 `notes` 文件夹，用于存放文档，新建 `pics` 文件夹，用于存放文档所需图片。在 `notes` 文件夹下新建文件 `1.1 操作系统的目标和作用.md`

  ```markdown
  <!-- 1.1 操作系统的目标和作用.md -->
  
  <div align="right"><a href="#README.md">返回目录</a></div>

  ## 1.1 操作系统的目标和作用
  &emsp;&emsp;目前存在着多种类型的OS，不同类型的OS，其目标各有所侧重。通常在计算机硬件上配置的OS，其目标是：方便性、有效性、可扩充性和开放性。
  <br><br>
  #### 一、OS作为用户与计算机硬件系统之间的接口

  &emsp;&emsp;其意义是：OS处于用户与计算机硬件系统之间，用户通过OS来使用计算机系统。或者说，用户在OS帮助下，能够方便、快捷、安全、可靠地操纵计算机硬件和运行自己的程序。应注意，OS是一个系统软件，因而这种接口是软件接口。

  <div align="center">
      <img src="/pics/1-1.png" width="400px">
  </div>

  &emsp;&emsp;用户可以通过三种方式使用计算机。（1）命令方式。这是指由OS提供了一组联机命令（语言），用户可通过键盘输入有关命令，来直接操纵计算机系统。（2）系统调用方式。OS提供了一组系统调用，用户可在自己的应用程序中通过相应的系统调用，来操纵计算机。（3）图形-窗口方式。用户通过屏幕上的窗口和图标来操纵计算机系统和运行自己的程序。
  <br><br>
  #### 二、OS作为计算机系统资源的管理者

  &emsp;&emsp;其意义是：在一个计算机系统中，通常都含有各种各样的硬件和软件资源。归纳起来可将资源分为四类：处理器、存储器、I/O设备以及信息（数据和程序）。<br/>
  &emsp;&emsp;相应地，OS的主要功能也正是针对这四类资源进行有效的管理，即：处理机管理，用于分配和控制处理机；存储器管理，主要负责内存的分配与回收；I/O设备管理，负责I/O设备的分配与操纵；文件管理，负责文件的存取、共享和保护。可见，OS确是计算机系统资源的管理者。事实上，当今世界上广为流行的一个关于OS作用的观点，正是把OS作为计算机系统的资源管理者。
  <br><br>
  #### 三、OS实现了对计算机资源的资源

  &emsp;&emsp;其意义是：对于一台完全无软件恶到计算机系统（即裸机），即使其功能再强，也必定是难于使用的。如果我们在裸机上覆盖上一层I/O设备管理软件，用户便可利用它所提供的I/O命令，来进行数据输入和打印输出。此时用户所看到的机器，将是一台比裸机功能更强、使用更方便的机器。通常把覆盖了软件的机器称为扩充机器或虚机器。<br>
  &emsp;&emsp;如果我们又在第一层软件上再覆盖上一层文件管理软件，则用户可利用该软件提供的文件存取命令，来进行文件的存取。此时，用户所看到的是台功能更强的虚机器。如果我们又在文件管理软件上再覆盖一层面向用户的窗口软件，则用户便可在窗口环境下方便地使用计算机，形成一台功能更强地虚机器。
  <br><br><br>
  &emsp;&emsp;推动操作系统发展的主要动力是：1.不断提高计算机资源利用率、2.方便用户、3.器件的不断更新换代、4.计算机体系结构的不断发展、5.不断提出新的应用需求。
  <br><br>
  <center>--end--</center>
  ```

<div align=right><a href="#简单入门指南">⬆ return to top</a></div>

### 完善 index.html

&emsp;&emsp;🎈 特别强调，我这里 copy 了 github 用户名为 [cyc2018](https://github.com/CyC2018/CS-Notes) 的样式。// 仰仗一波大佬

  ```html
  <!-- index.html -->

  <!DOCTYPE html>
  <html lang="en">

  <head>
      <meta charset="UTF-8">
      <title>计算机操作系统</title>
      <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
      <meta name="description" content="Description">
      <meta name="viewport" content="width=device-width, user-scalable=yes, initial-scale=1.0, maximum-scale=2.0, minimum-scale=1.0">
      <link rel="icon" href="_media/icon3.png">
      <link rel="stylesheet" href="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/vue.css">
      <!-- 将自定义样式放在 Github 上会导致加载速度变得非常慢，所以采取直接内嵌的方式 -->
      <style type="text/css">
      /* 隐藏头部的目录 */
      #main>ul:nth-child(1) {
          display: none;
      }
      #main>ul:nth-child(2) {
          display: none;
      }
      h1+ul {
          display: block !important;
      }
      .markdown-section h1 {
          margin: 3rem 0 2rem 0;
      }
      .markdown-section h2 {
          margin: 2rem 0 1rem;
      }
      img,
      pre {
          border-radius: 8px;
      }
      .content,
      .sidebar,
      .markdown-section,
      body,
      .search input {
          background-color: rgba(243, 242, 238, 1) !important;
      }
      @media (min-width:600px) {
          .sidebar-toggle {
              background-color: #f3f2ee;
          }
      }
      .docsify-copy-code-button {
          background: #f8f8f8 !important;
          color: #7a7a7a !important;
      }
      body {
          /*font-family: Microsoft YaHei, Source Sans Pro, Helvetica Neue, Arial, sans-serif !important;*/
      }
      .markdown-section>p {
          font-size: 16px !important;
      }
      .markdown-section pre>code {
          font-family: Consolas, Roboto Mono, Monaco, courier, monospace !important;
      }
      @media (min-width:600px) {
          .markdown-section pre>code {
              font-size: .9rem !important;
          }
      }
      @media (max-width:600px) {
          .markdown-section pre>code {
              padding-top: 5px;
              padding-bottom: 5px;
          }
          pre:after {
              content: "" !important;
          }
      }
      /*.anchor span {
      color: rgb(66, 185, 131);
      }*/
      section.cover h1 {
          margin: 0;
      }
      body>section>div.cover-main>ul>li>a {
          color: #42b983;
      }
      .markdown-section > div > img,
      .markdown-section pre {
          box-shadow: 2px 2px 20px 6px #ddd !important;
      }
      pre {
          background-color: #f3f2ee !important;
      }
      @media (min-width:600px) {
          pre code {
              /*box-shadow: 2px 1px 20px 2px #aaa;*/
              /*border-radius: 10px !important;*/
              padding-left: 20px !important;
          }
      }
      @media (max-width:600px) {
          pre {
              padding-left: 0px !important;
              padding-right: 0px !important;
          }
          .docsify-copy-code-button {
              display: none;
          }
      }
      .markdown-section pre {
          padding-left: 0 !important;
          padding-right: 0px !important;
      }
      </style>
      <style type="text/css">
      /**
   * prism.js Coy theme for JavaScript, CoffeeScript, CSS and HTML
   * Based on https://github.com/tshedor/workshop-wp-theme (Example: http://workshop.kansan.com/category/sessions/basics or http://workshop.timshedor.com/category/sessions/basics);
   * @author Tim  Shedor
   */
      code[class*="language-"],
      pre[class*="language-"] {
          color: black;
          background: none;
          font-family: Consolas, Monaco, 'Andale Mono', 'Ubuntu Mono', monospace;
          text-align: left;
          white-space: pre;
          word-spacing: normal;
          word-break: normal;
          word-wrap: normal;
          line-height: 1.5;
          -moz-tab-size: 4;
          -o-tab-size: 4;
          tab-size: 4;
          -webkit-hyphens: none;
          -moz-hyphens: none;
          -ms-hyphens: none;
          hyphens: none;
      }
      /* Code blocks */
      pre[class*="language-"] {
          position: relative;
          margin: .5em 0;
          overflow: visible;
          padding: 0;
      }
      pre[class*="language-"]>code {
          position: relative;
          border-left: 10px solid #358ccb;
          box-shadow: -1px 0px 0px 0px #358ccb, 0px 0px 0px 1px #dfdfdf;
          background-color: #fdfdfd;
          background-image: linear-gradient(transparent 50%, rgba(69, 142, 209, 0.04) 50%);
          background-size: 3em 3em;
          background-origin: content-box;
          background-attachment: local;
      }
      code[class*="language"] {
          max-height: inherit;
          height: inherit;
          padding: 0 1em;
          display: block;
          overflow: auto;
      }
      /* Margin bottom to accommodate shadow */
      :not(pre)>code[class*="language-"],
      pre[class*="language-"] {
          background-color: #fdfdfd;
          -webkit-box-sizing: border-box;
          -moz-box-sizing: border-box;
          box-sizing: border-box;
          margin-bottom: 1em;
      }
      /* Inline code */
      :not(pre)>code[class*="language-"] {
          position: relative;
          padding: .2em;
          border-radius: 0.3em;
          color: #c92c2c;
          border: 1px solid rgba(0, 0, 0, 0.1);
          display: inline;
          white-space: normal;
      }
      pre[class*="language-"]:before,
      pre[class*="language-"]:after {
          content: '';
          z-index: -2;
          display: block;
          position: absolute;
          bottom: 0.75em;
          left: 0.18em;
          width: 40%;
          height: 20%;
          max-height: 13em;
          box-shadow: 0px 13px 8px #979797;
          -webkit-transform: rotate(-2deg);
          -moz-transform: rotate(-2deg);
          -ms-transform: rotate(-2deg);
          -o-transform: rotate(-2deg);
          transform: rotate(-2deg);
      }
      :not(pre)>code[class*="language-"]:after,
      pre[class*="language-"]:after {
          right: 0.75em;
          left: auto;
          -webkit-transform: rotate(2deg);
          -moz-transform: rotate(2deg);
          -ms-transform: rotate(2deg);
          -o-transform: rotate(2deg);
          transform: rotate(2deg);
      }
      /*黑色*/
      .token.function,
      .token.operator,
      .token.class-name {
          color: #2C3E50;
      }
      /*深蓝加粗*/
      .token.keyword {
          color: #124363;
          font-weight: bold;   
      }
      /*浅蓝*/
      .token.property,
      .token.tag,
      .token.boolean,
      .token.number,
      .token.function-name,
      .token.constant,
      .token.symbol,
      .token.deleted {
          color: #2980B9;
      }
      .token.comment,
      .token.block-comment,
      .token.prolog,
      .token.doctype,
      .token.cdata {
          color: #7D8B99;
      }
      .token.punctuation {
          color: #5F6364;
      }
      .token.selector,
      .token.attr-name,
      .token.string,
      .token.char,
      .token.builtin,
      .token.inserted {
          color: #1ABC9C;
          font-weight: bold;   
      }
      .token.entity,
      .token.url,
      .token.variable {
          color: #a67f59;
          /*background: rgba(255, 255, 255, 0.5);*/
      }
      .token.atrule,
      .token.attr-value {
          color: #1990b8;
      }
      .token.regex,
      .token.important {
          color: #e90;
      }
      .language-css .token.string,
      .style .token.string {
          color: #a67f59;
          background: rgba(255, 255, 255, 0.5);
      }
      .token.important {
          font-weight: normal;
      }
      .token.bold {
          font-weight: bold;
      }
      .token.italic {
          font-style: italic;
      }
      .token.entity {
          cursor: help;
      }
      .namespace {
          opacity: .7;
      }
      @media screen and (max-width: 767px) {
          pre[class*="language-"]:before,
          pre[class*="language-"]:after {
              bottom: 14px;
              box-shadow: none;
          }
      }
      /* Plugin styles */
      .token.tab:not(:empty):before,
      .token.cr:before,
      .token.lf:before {
          color: #e0d7d1;
      }
      /* Plugin styles: Line Numbers */
      pre[class*="language-"].line-numbers.line-numbers {
          padding-left: 0;
      }
      pre[class*="language-"].line-numbers.line-numbers code {
          padding-left: 3.8em;
      }
      pre[class*="language-"].line-numbers.line-numbers .line-numbers-rows {
          left: 0;
      }
      /* Plugin styles: Line Highlight */
      pre[class*="language-"][data-line] {
          padding-top: 0;
          padding-bottom: 0;
          padding-left: 0;
      }
      pre[data-line] code {
          position: relative;
          padding-left: 4em;
      }
      pre .line-highlight {
          margin-top: 0;
      }
      </style>
  </head>

  <body>
      <div id="app"></div>
      <script>
      window.$docsify = {
          maxAge: 100,
          name: '章节目录',
          repo: 'https://github.com/fmw666/Operating-System',
          search: {
              paths: 'auto',
              placeholder: '🔍 Type to search ',
              noData: '😞 No Results! ',
              depth: 6
          },
          // subMaxLevel: 2,
          coverpage: true
      }
      </script>
      <script src="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/docsify.min.js"></script>
      <script src="https://cdn.bootcss.com/docsify/4.5.9/plugins/search.min.js"></script>
      <script src="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/docsify-copy-code.min.js"></script>
      <script src="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/prism-java.min.js"></script>
      <script src="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/prism-c.min.js"></script>
      <script src="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/prism-bash.min.js"></script>
      <script src="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/prism-sql.min.js"></script>
      <script src="https://cyc-1256109796.cos.ap-guangzhou.myqcloud.com/zoom-image.min.js"></script>
      <!-- <script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script> -->
  </body>

  </html>
  ```

<div align=right><a href="#简单入门指南">⬆ return to top</a></div>
