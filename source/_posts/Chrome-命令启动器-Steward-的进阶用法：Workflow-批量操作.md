---
title: Chrome 命令启动器 Steward 的进阶用法：Workflow 批量操作
date: 2018-04-30 18:30:26
reward: true
tags: 
- Steward
- 效率
- Workflow
---

此 Workflow 非大家熟知的 iOS 自动化工具，而是 Chrome 效率插件 Steward 里的一个进阶功能，可以用一条简单的命令代替原先繁琐、重复的操作，节省大量时间，同时还能拯救鼠标。



在[之前的文章](https://sspai.com/post/42121)里，我介绍了 Steward 的三种模式，而有了 Workflow，Steward 的使用就更简单了。



Steward 是开源项目，代码托管在 [Github](https://github.com/solobat/Steward) 上，从 [Chrome应用商店](https://chrome.google.com/webstore/detail/dnkhdiodfglfckibnfcjbgddcgjgkacd) 安装，或 [离线下载](http://owsjc7iz3.bkt.clouddn.com/steward-3.3.crx)，官网是[oksteward.com](http://oksteward.com/)。

## Steward 的 Workflow 是什么

开发 Workflow 功能的动力就来自我自己的生活。每天我都会打开相对固定的几个网页浏览资讯，而作为一个 Chrome 用户，我还安装了许多插件，根据不同使用场景频繁禁用、启用。按传统的方式，这些操作总是免不得每次都得**用鼠标点击多次**或者按多个快捷键，操作一多，感觉**手累**还容易有所遗忘。



之前我就做了一个 Chrome 效率插件 Steward，在觉察到频繁操作的痛点后，我重构了程序的主流程，使之能一次执行多条命令，并给出相应的提示，Workflow 功能就这样诞生了。

## Workflow 能做什么

在讲解 Workflow 怎么用之前，先通过几个很常见的场景来告诉大家 Workflow 能做什么，具体命令请看文章末尾的附录部分。

<!-- more -->

### 打开多个网址

> 每天上班到公司，先刷一遍常用网站才能安心开始工作



#### 创建

名称随意，比如「科技产品以及论坛」，每一行都是一个你的常用网址。

#### 使用

在任意模式的 Steward 输入框输入：`wf keji` 或者 `wf kjcp` 等与 workflow 名称有关的拼音字母、汉字、英文的简写组合形式。

![Workflow 动图](https://cdn.sspai.com/2018/01/12/f13faff1ab7efdb9662904611d5a8a47.gif)

### 扩展批量管理

> 我在家与在公司需要的扩展是不同的，怎么才能快捷、方便的批量处理呢？



#### 批量禁用 -- 「禁用所有扩展」

![一键禁用所有扩展](https://cdn.sspai.com/2018/01/12/41cecb29daeee79c98d6e0a7d9435528.gif)

#### 批量启用「常用扩展」

![批量启用常用扩展](https://cdn.sspai.com/2018/01/12/b3d28589a8447bf69ff2f2c4fb1259bf.gif)

### 网站批量屏蔽与解锁

> 现在上班时间容易注意力不集中，没几分钟就想刷一波网站，怎么才能管住这不听话的鼠标呢？



#### 批量屏蔽的 workflow -- 「屏蔽网站」

![批量屏蔽网站论坛](https://cdn.sspai.com/2018/01/12/a83519824a3adfe9dd98c95ac3cd3288.gif)

#### 批量解锁的 workflow -- 「解除屏蔽」

![一键解锁屏蔽的网站](https://cdn.sspai.com/2018/01/12/86a955f0061ac6c864064e79f6320baf.gif)



> 我想既禁用所有扩展，同时还要屏蔽一些网站，按你上面的例子，需要用2条命令才行啊，效率还有提高空间吧？



当然的，Steward v3.2.1 以后，正式支持 Workflows 的组合，创建一个名为「开始工作」的 workflow，内容里包含「禁用所有扩展」、「屏蔽网站」两个 Workflow ，这样就能一条命令搞定所有操作：

![Workflows 的组合](https://cdn.sspai.com/2018/01/12/077f708b715aa55399ae6ebdebc927b2.gif)

## Workflow 怎么用

上面是 Workflow 在常用场景下的典型实例，为了充分利用 Workflow 的强大能力，有必要了解下它的一些规则。



### 创建

> Workflow 本质上是多条经过增强的**命令**：命令的要求是能在 Steward 输入框里执行，如果达不到目的，就需要一些增强的语法。



在设置 -> Workflows 面板点击`+ New Workflow`按钮，然后在右侧的表单中填写，其中`Title`和`Content`字段是必填的


`Content` 的填写需要遵循一点简单的语法:

基本格式： `command|numbers` 

* `command` 是必填的，由 `trigger` + `空格` + `query` 组成，注意不要忘记**空格** 

* `numbers` 是可选的，表示前面的 `command` 所将作用的条目的数量，只对 `trigger` 后面带 `batch` 图标的 command 有效 



以上只是语法的一部分，同时也是最有用的，了解这些已经够用了，更多请看官方[帮助文档](http://oksteward.com/steward-document-zh/Workflows.html#%E5%88%9B%E5%BB%BA)



![Workflows](https://cdn.sspai.com/2018/01/12/6bd73f3738311ae16cb9151bd8bba46d.png)




### 使用

在命令框中输入`wf `将列出所有的 `workflow`, 选中后按 `Enter/Return` 将执行 `workflow`, 完成后将会有 `Toast` 显示执行的各条命令



## 附录命令

### 「科技产品以及论坛」

```

36kr.com

ifanr.com

sspai.com

www.producthunt.com

next.36kr.com/posts

www.appinn.com

zhihu.com

v2ex.com

```

### 「禁用所有扩展」

```

off |all

```

### 「常用扩展」

```

on adblock

on vimium

on dancixiaokapian

on 1password

on stylish

on jianyue

```

### 「屏蔽网站」

```

bk zhihu.com

bk toutiao.com

bk jandan.net

bk douban.com

```

### 「解除屏蔽」

```

bk |all

```

### 「开始工作」

```

wf 屏蔽

wf 禁用

```

> 虽然 Steward Workflow 已经很方便了，但不可否认它还有的改进空间。我已经有了一些规划，敬请关注。


