---
title: Steward -- 一款 Chrome 上的类 Alfred / Wox 启动器，键盘党的效率神器
date: 2017-12-13 17:44:14
reward: true
tags: 
- Steward
- 效率
---

说到启动器，最有名的当属 Mac 上的神器 Alfred ，以及 Windows 上的 Wox。那什么是启动器呢，它是由一个命令输入框，以及一个查询结果下拉列表组成。只需要一个命令就能让电脑去完成一系列操作，如同你的管家一样，自然是很多人心目中的神器。



比如我输入 `Chrome` 然后回车，启动器会自动帮我找到 Chrome 并打开它；又如遇到命令 `yd steward` 后，启动器立刻去查询有道词典然后把 `管家` 的释义列出来。



而 Steward 便是 Chrome 浏览器里的类 Alfred 启动器，在某些方面甚至是 Alfred Plus。

## 概述

在 Chrome 中，通过 Steward 简单地输入某些命令，就能完成扩展、书签、标签页管理等大部分浏览器操作。  



Steward 是开源项目，代码托管在 [Github](https://github.com/solobat/Steward) 上，从 [Chrome应用商店](https://chrome.google.com/webstore/detail/dnkhdiodfglfckibnfcjbgddcgjgkacd) 安装，或 [离线下载](http://owsjc7iz3.bkt.clouddn.com/steward-3.1.5.crx)，官网是[oksteward.com](http://oksteward.com/)。



先来一手举一个栗子：

> 我感觉到逛知乎、头条、煎蛋等网站的时间太多了，以致于没法专心工作学习，可总是手贱管不住鼠标，肿么办！？   



只要在 Steward 的命令框里分别输入以下几条命令

```

bk zhihu.com

bk toutiao.com

bk jandan.net

```

那么这些网站将无法正常访问，除非你手动解除屏蔽；如果你觉得这还不够彻底，可以用强制屏蔽8小时的 `bk8` 命令。妈妈再也不用担心我的工作学习了！    



更厉害的栗子：

> 我每天必刷各种科技、互联网的文章资讯，可是网站那么多，要一个一个打开，手累！还可能会有所遗忘，如何是好？！



这样做就好，使用 Steward 创建一个 workflow，标题就叫做 `科技互联网资讯`：

```

sspai.com

36kr.com

ifanr.com

readhub.me

donews.com

```

在命令框里输入 `wf kjhlwzx` 或者 `wf 科技` 甚至 `wf kj` ，然后回车，刷刷刷，这些网站全都依次打开了。    

![动图](https://user-gold-cdn.xitu.io/2017/12/13/1604e26b5b74e1d4?w=2560&h=1556&f=gif&s=1861559)

 

大概你也发现了，第一个栗子也是可以做成 workflow 的，怎么样，有没有初步感觉到浏览器已经**被你支配**了？



Steward 是可以比拟 AdBlock、 Stylish、Vimium 这等 Chrome 神器的，至于为什么，先不说它的[帮助文档](https://steward-launcher.github.io/steward-document-zh/)丰富得吓人，看看它的进化之路吧。   



> 什么鬼？我才不关心进化之路什么的。



没关系，可以直接看看图，然后就你明白了。 



## 缘由

个人挺喜欢收集各种扩展，可安装多了，管理就是一个麻烦。尝试过 Chrome 应用商店的诸多扩展管理类工具，始终不尽如人意。



早在 2014 年底，作为一个效率控，凑巧又是一个刚用上 MBP 的前端工程师，受 Alfred 启发，开发了 Steward 这样一款浏览器里的命令启动器。

## 开发

### 初始

第一版很简陋，花了一个晚上，只有个简单的 `popup` 弹框，以及两个 `plugin` 组成的插件系统： `on` 启用扩展，`off` 禁用扩展。

此时的名字还不是 Steward，而是 Ikkyu，即聪明的「一休」的英文名。

虽然有点小激动，毕竟自己的第一个作品，但旅途才刚刚开始。

### 支持拼音

首先，作为中国人，不支持`中文拼音`搜索怎么行，所以使用 [pinyin](https://github.com/hotoo/pinyin) 来支持。

### 厚积

接下来就是漫长的各种 plugin 的发现与开发之旅，就像沙滩上捡贝壳的小孩儿一样，每遇到一个 idea，就惊喜莫名，要立刻实现它，即使会遇到各种困难。

从 Github 的`commit`记录上可以看到走过的每一步：

- `yd`: 有道查词, `his`: 历史记录查询, `todo`: 待办事项

- `run`: 启动应用, `po`: pocket 文章查询, `del`: 扩展删除

- `bm`: 书签查找，`set`: 打开扩展的设置，`bk`: 屏蔽网站

- `dl`: 下载记录，`help`：帮助命令



![众多插件](https://user-gold-cdn.xitu.io/2017/12/13/1604e26b5873fa79?w=2556&h=1366&f=jpeg&s=311047)



### 支持新标签页

在某一天突然想到，这么常用的功能，为什么不放在 New Tab（新标签页） 呢？

于是就开启了三大使用模式之二 **New Tab模式** 的篇章

### 壁纸

发现有些难看，怎么办？

果断加上了来自 Bing 的壁纸，每天一张，自动刷新。

此时，Steward 像是完成了自我发现，开始走进朋友、同事的视野。

### 迷茫

直到2017年某天，看着眼前的 Steward，猛然发现它跟我一样已经停滞不前了。

收拾好心绪，带着这种不安，开始了与 Steward 的重生之路。

### 重生

在某只小青蛙的鼓励帮助下，从 UI 开始，换掉原来的圆角输入框，一下子让 Steward 显得轻松了很多。

试着向外推荐了一下，看着 Chrome 扩展后台用户的陡然提升，感觉全都回来了

### 薄发

在深入体验了 `Alfred` 以及类似命令启动器以后发现了一些共同点，都是 `Steward` 应该有但还没有的。

v2.5 设置页面到来，自此可以**自定义** `plugin` 里各 `command` 的 `trigger`（触发条件）。

在完善了帮助说明以后，某天发现遇到好看的壁纸却无可奈何！

紧接着，添加壁纸`save`按钮，以及在设置面板中可以对壁纸设置、下载、删除。



![壁纸](https://user-gold-cdn.xitu.io/2017/12/13/1604e26b596e9e12?w=2558&h=1376&f=jpeg&s=540752)

v2.6 天气查询、网址输入、搜索引擎查找，应有的功能逐步补齐。



v2.7 三大模式之「页面模式」到来，在任何页面都能用快捷键唤起 Steward。



![页面模式-使用 site 命令查看常用网站](https://user-gold-cdn.xitu.io/2017/12/13/1604e26b67b6bac0?w=2558&h=1368&f=jpeg&s=890966)

v2.8 加入几乎所有的 Chrome 浏览器原生页面 url，以后无论想打开 bookmarks 、help 还是 settings 等等菜单或页面，也就一句命令的事儿。

![Chrome 页面](https://user-gold-cdn.xitu.io/2017/12/13/1604e26b5e7ed099?w=2558&h=1372&f=png&s=1218399)



v2.9 新增扩展类`plugin`，在 Steward 里与其它扩展交互(`单词小卡片`)，可以说是在扩展界是   Steward 独有的功能，因为它们都有同一个作者。



v3.0的大改进导致了 Steward 偶尔出一些问题，以致于作者「半夜」还在修复中，然而似乎也在预示着更大的高潮。



到达 v3.0 的 Steward 可以说已经是准神器了，直到 v3.1 在启动器界具有 Steward 特色的功能 Workflows 闪亮登场。

从此 Steward 告别了一次只能执行一个操作/一条命令的局限，开始具有无限的可能，完全具备了效率神器的资格，有资格称为 Chrome 上的 Alfred Plus。当然，这还需要时间去沉淀，也需要用户去探索。



![创建 workflow](https://user-gold-cdn.xitu.io/2017/12/13/1604e26b5a807ac2?w=2556&h=1362&f=jpeg&s=338108)

v3.1.2到来的 `random` 插件，看似不起眼，却使 Steward 超越了传统的「New Tab」类扩展，新标签不再仅仅只是一个花瓶，比如它可以同时扮演 TodoList、书签管理、背单词等角色。



## 其它

Steward 功能图示

![Steward 功能图示](https://user-gold-cdn.xitu.io/2017/12/13/1604e26b9e67d1a6?w=2021&h=2576&f=png&s=356664)



Steward 是个人的第一个开源项目，因而从开源社区学习到了很多东西。

- 技术栈：`Webpack + Vue2`，当然也有 `jQuery`、`pinyin` 这样的库

- 设计：不懂设计，怎么办呢？设置页面用的 `ElementUI`，图标大都来自  [iconfont.cn](iconfont.cn)

- 产品：从[简悦](https://github.com/Kenshin/simpread)以及其它一些优秀的开源项目学习了怎么维护一个产品。当然目前 `Steward` 还做得不够



向上面提到的这些项目及作者表示感谢。



## 关于未来

自我觉得给 Steward 赋予了极大的可能性，目前有、将来也会有很多 idea 在上面展示以及探索；

与 Steward 同源，但没有新标签页模式的 **Browser Alfred** 则会同步更新相应的功能。

> 关注 Steward，关注它的一切，就等于关注了更有效率。

