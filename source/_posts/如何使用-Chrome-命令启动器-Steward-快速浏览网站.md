---
title: 如何使用 Chrome 命令启动器 Steward 快速浏览网站
date: 2018-04-30 18:32:40
reward: true
tags: 
- Steward
- 效率
---
在[之前的文章](https://sspai.com/post/42121)里，我介绍了 Steward 的三种模式，这篇文章将介绍如何利用三种模式快速浏览网站与网页。



Steward 是开源项目，代码托管在 [Github](https://github.com/solobat/Steward) 上，从 [Chrome应用商店](https://chrome.google.com/webstore/detail/dnkhdiodfglfckibnfcjbgddcgjgkacd) 安装，或 [离线下载](http://owsjc7iz3.bkt.clouddn.com/steward-3.3.2.crx)，官网是[oksteward.com](http://oksteward.com/)，也有官方论坛[bbs.oksteward.com](http://bbs.oksteward.com)。

<!-- more -->

## 访问整个网络 — 多命令

此功能可以在 Steward 的任意模式中使用。



### 书签

命令：`bm`

![支持书签的查找与打开](https://cdn.sspai.com/2018/02/28/aee189d87975e68189b632eca5d8052d.gif)



### 历史记录

命令:  `his`

![支持历史记录的查找与打开](https://cdn.sspai.com/2018/02/28/26caef9db75093dccb8dad45da9ac077.gif)



### 最常访问

命令：`site`

由于 Steward 会占用新标签页，因此提供 `site` 命令查看 Chrome 原生新标签上显示的最常访问网站列表。

![查看常用网站并打开](https://cdn.sspai.com/2018/02/28/2248ef5ea3d12f4a201d662becd0498b.gif)



### 直接输入链接

直接在 Steward 输入框输入你要访问的网站  URL，按 Enter / Return 键即可。

![输入网站域名并打开](https://cdn.sspai.com/2018/02/28/7628b34aa8858044e7c27081fdc22de7.gif)



### 使用搜索引擎

当你的输入没有匹配到任何内容时，Steward 会列出搜索引擎列表，选择后会跳转到指定网站的搜索页面



#### 搜索引擎设置

命令：`se`



![多引擎搜索与引擎设置](https://cdn.sspai.com/2018/02/28/a4a283dbd9ef43c42207690598272eba.gif)



## 站点访问 — 导航

通常要访问站点内的其它特定页面，只能手动输入链接或点击什么一下。虽然 Vimium / Surfingkeys 的 `F` 键能快速打开页面内的链接，但往往需要输入 2、3 个无意义的字母，感觉不太方便，而且它只能查找页面内可见区域的链接，对于不可见的就无能为力了。



此功能需要在 Steward 的**页面模式**中使用，即通过页面模式快捷键唤起 Steward 输入框。



### 站点配置

在选项 -> Websites 面板进行管理

以少数派举例创建一个 Website:

![创建 Website](https://i.imgur.com/c1xCfwY.png)



#### 自定义 Paths

考虑到一个网站的网站地图变化不会太大，所以想到可以为指定站点添加一些常用页面，通过 Steward 来快速访问。



比如我想添加少数派的个人主页，只需要在 Paths 处分别输入 title: 个人主页，path: `/user/784469/updates` ，点击 + 按钮即可。



#### 自动提取导航

开发过程中，发现很多网站页面都是有导航区域存在的，这里面的链接通过简单地指定 **css selector** 就可以提取出来。



对于符合 HTML5 规范的站点/页面，默认的 `nav a`就基本满足；对于其它站点/页面，了解 css 的同学可以通过 Chrome DevTools 查看，不了解 css 也没关系，可以去[Steward：中文社区](http://bbs.oksteward.com/)发贴或在 [Telegram 交流群](https://t.me/chromesteward)中求助。





![页面模式使用导航](https://cdn.sspai.com/2018/02/28/b87e9c0db6220131e3f5942a0829c616.gif)



## 页面浏览 — 大纲/outline

当我们浏览篇幅较长的文章时，往往需要反复地**快速定位**到文章内的某些部分，虽然一些扩展支持自动提取页面大纲，但基本都做不到配置灵活与快速定位。而 Steward 作为一个浏览器启动器，天然地适合这份工作。



以少数派文章举例，只需要在少数派的 Website 配置里将 Outline Scope 字段填充为`.article-content`并保存即可。



![页面模式中使用 outline](https://cdn.sspai.com/2018/02/28/3ceca70fc29892edbf1fa5d2b4c5ced6.gif)



## 说明

目前 Steward 的 Websites 功能还在进一步探索与完善中，后续陆续会加入类似站点配置导入、导出，站点配置分享，页面内 Buttons 点击等功能，敬请期待。

