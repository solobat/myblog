---
title: Steward 攻略之扩展管理篇
date: 2018-04-30 18:33:58
reward: true
tags: 
- Steward
- 效率
---
Steward 作为一个浏览器启动器，你可以通过输入某些命令，就能完成扩展、书签、标签页管理等大部分浏览器操作。



而开发 Steward 的初衷其实是为了方便禁用、启用扩展，当然对扩展的管理不只这二种，这篇攻略将为大家详细介绍一下。



Steward 是开源项目，代码托管在 [Github](https://github.com/solobat/Steward) 上，从 [Chrome应用商店](https://chrome.google.com/webstore/detail/dnkhdiodfglfckibnfcjbgddcgjgkacd) 安装，或 [离线下载](http://owsjc7iz3.bkt.clouddn.com/steward-3.4.2.crx)，官网是[oksteward.com](http://oksteward.com/)，论坛是[bbs.oksteward.com](http://bbs.oksteward.com/)。

<!-- more -->


## 启用扩展

命令：`on`

![on 命令启用扩展](https://cdn.sspai.com/2018/04/01/14ca5c601d8eb1dcd789d56a45fc00f8.gif)



### 批量启用

使用命令启用扩展是挺方便的，但缺点在于只能针对单个扩展，而通过创建 Workflow 则可以批量启用扩展(详见附录)。

![批量启用扩展](https://cdn.sspai.com/2018/04/01/52a9cd2068f8915f3c04c143af77b0c3.gif)



## 启动应用

命令：`run`

![run 命令打开应用](https://cdn.sspai.com/2018/04/01/87bbfe85b62445b1a237293e47cb810d.gif)



## 禁用扩展

命令：`off`

![off 命令禁用扩展](https://cdn.sspai.com/2018/04/01/4f6ee72ee937e46103a00d0753f23e7c.gif)



### 一键禁用

同样，使用 Workflow 可以一键禁用所有扩展(详见附录)。

![一键禁用所有扩展](https://cdn.sspai.com/2018/04/01/3279d0d93509d7d0230355db97a2f60d.gif)



上述命令会将除 Steward 之外的所有扩展禁用，如果要更彻底一些，可以在 Workflow 中加上 `off Steward` 命令。



## 删除扩展

命令：`del`

![del 命令删除扩展](https://cdn.sspai.com/2018/04/01/8786e41e91a492da93cbe5f107470bd9.gif)



## 设置扩展

通常，每个扩展都有一个设置页面，以往我们只能点击扩展右键菜单中的选项打开它。

命令：`set`

![set 命令设置扩展](https://cdn.sspai.com/2018/04/01/1452d93d74707fa2e0a701dc3bae81e0.gif)



## 查看扩展

命令：`ext` 查看浏览器中的扩展详情

![ext 命令查看浏览器中的扩展详情](https://cdn.sspai.com/2018/04/01/1ed78fc2ffbbfdb76e3b9d266387c44d.gif)



按住 `Shift` 时，将打开扩展的主页，通常是 Chrome WebStore 详情或扩展的官网。

![ext 命令 Shift + Enter 打开扩展主页](https://cdn.sspai.com/2018/04/01/bbf5d7550cc8901b1d4067825ab1441d.gif)



## 扩展协作

除了对扩展进行管理外，Steward 还能与某些扩展进行协作交互，前提是这些扩展有开放的接口。



以[单词小卡片扩展](https://chrome.google.com/webstore/detail/%E5%8D%95%E8%AF%8D%E5%B0%8F%E5%8D%A1%E7%89%87-%E6%9F%A5%E8%AF%8D%E6%94%B6%E9%9B%86%E8%83%8C%E5%8D%95%E8%AF%8D/oegblnjiajbfeegijlnblepdodmnddbk)为例 -- 它是我的另一款[开源](https://github.com/solobat/wordcard)浏览器扩展，为了配合 Steward 而提供了对外接口。

![单词小卡片扩展](https://cdn.sspai.com/2018/04/01/4a532f7ec7cf7e4d82e878c97ec25f7c.gif)



单词小卡片扩展支持单词查询、例句收集、卡片制作以及背单词功能。为了**更便捷**的背单词，我开放了一个相应的 Steward 插件，命令为 `wd`。

![wd 命令背单词](https://cdn.sspai.com/2018/04/01/5a8bc600e3780aea6a99b9d499c6d3ca.gif)



如果你对于其它扩展也有类似的需求，可以去请求它的开发者提供对外接口，之后我就可以为其开发一个相应的插件与之配合使用。



## 附录

### 批量启用扩展的 Workflow

```

on vimum

on stylish

on simread

on save to pocket|2

on adblock|2

on dancixiaokapian|2

on 1password

on weibotuchuang

```



### 禁用所有扩展(Steward 除外)

```

off |all

```



### 禁用所有扩展

```

off |all

off Steward

```



## 延伸阅读

[在 Chrome 里用「Alfred」是什么体验？Steward 把效率启动器带进了浏览器](https://sspai.com/post/42048)



[Chrome 命令启动器 Steward 的进阶用法：Workflow 批量操作](https://sspai.com/post/42088)

