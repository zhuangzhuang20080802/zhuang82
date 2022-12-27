---
title: Tor~
date: 2022-12-27 07:33:12
tags: ["技术与生活","OverGFW"]
---

### 前言

前几天那场考试，我写了一篇名为《触摸现实》的作文，讲的就是我从进入暗网到逃离暗网的经过，在那里我把暗网描述为一个十分黑暗的地方，实际上我是很违心的，写成这样完全是题目和法律的要求。

### 概念

首先我们来了解一下什么是暗网。这个在之前那篇[我的Go-pass-GFW简史](https://zhuang82.tk/2022/12/11/%E6%88%91%E7%9A%84Go-pass-GFW%E7%AE%80%E5%8F%B2/)中提到过，但说实在，那篇文章我说的都不太对。

1. 广义上来说，不是所有人都能访问的（常规搜索引擎无法找到的），都可以以暗网称之。

2. 狭义上来说，暗网指Tor网络中的洋葱服务（`.onion`网址）

明网上有很多关于暗网的文章，大多贬低暗网，主要有两种：

[暗网是什么？为何亲历者都闭口不谈？它远比你了解的更恐怖_腾讯新闻](https://new.qq.com/omn/20220308/20220308A0AYYC00.html)

[带你见识真正的地狱：暗网人口黑市](https://zhuanlan.zhihu.com/p/57243084)

第一种比较笼统，他们的作者大多应该没进过，只是把听说或收集到的写了出来。

第二种比较具体，作者可能对某方面有了解，但太片面。

还是下面几段选自<https://support.torproject.org/>（国内无法访问）的文字比较客观：

> “Tor” 这一名称可用于多个不同的组件。
> 
> Tor 是一个您能运行在您的电脑上，保护您在互联网上安全的程序。
> 它会将您的通信在一个由多个中继站组成的分散网络内不断传递，这些中继站被来自世界各地的志愿者们运营，并以此来保护您：这阻止了某些人通过您访问了哪些网址来得知您的网络链接，也防止了您访问的网站获取您的地理位置。
> 这些由志愿者搭建的中继被成为 Tor 网络。
> 
> 大多数人通过 Tor 浏览器使用 Tor。它是一个基于火狐浏览器开发的版本，并修复了许多隐私问题。
> 您可以在我们的[关于页面](https://www.torproject.org/about/history/)了解更多信息。
> 
> Tor 项目是一个非盈利性（慈善）组织，它维护和开发 Tor 软件。

> 洋葱服务允许人们匿名的访问和发表信息，包括架设匿名网站。
> 
> 洋葱服务还被依赖于提供一系列的服务：去元数据式的聊天，文件共享，利用诸如[SecureDrop](https://securedrop.org/) 或[洋葱共享](https://onionshare.org/) 进行的记者之间的互动和资源共享，更安全的软件升级，和更安全的访问如 [Facebook](https://www.facebook.com/notes/protect-the-graph/making-connections-to-facebook-more-secure/1526085754298237/) 这样网页的渠道。
> 
> These services use the special-use top level domain (TLD) .onion 
> (instead of .com, .net, .org, etc.) and are only accessible through the 
> Tor network.
> 
> When accessing a website that uses an onion service, Tor Browser will
>  show at the URL bar an icon of an onion displaying the state of your 
> connection: secure and using an onion service.
> 
> To learn more about onion services, read [How do Onion Services work?](https://community.torproject.org/onion-services/overview/)

> “嗨！我正在使用 Tor 浏览器访问 xyz.com ，不过似乎你们并没有允许 Tor 用户访问。
> 我建议您重新考虑这个决定；Tor 被世界各地的人用来保护隐私和对抗审查。
> 封锁 Tor 用户意味着也可能封锁了希望在专制国家自由的浏览互联网的用户，希望隐藏自己避免被发现的研究人员、记者、举报人和社会活动家，或只是希望不被第三方跟踪的普通人。
> 请采取强硬立场支持数字隐私和互联网自由，以及允许 Tor 用户访问 xyz.com，谢谢。”

> Tor 被设计成通过防止被各种人（甚至是我们）监控和审查来抵御人权和隐私。
> 我们厌恶用 Tor 做糟糕的事情的人，但是我们并不能在剔除他们的同时，不伤害到人权活动者，记者，虐待后的幸存者们，以及其他用 Tor 做好事的人们。
> 虽然我们仅需要增加一些软件后门就可以阻止某些人使用 Tor 网络，但是这会导致我们的用户遭更容易受到专制政权和其他组织的攻击。

**（本意是好的，只是被滥用了而已）**

### 实践

**在上面那段浓墨重彩的叙述后，这一段好像都不怎么重要了**

实际上现在进入暗网已经相当简单了，只需要Tor Browser这个浏览器，配置网桥。[https://support.torproject.org/](https://support.torproject.org/)有详细介绍，可惜已经被墙。

为了方便大家，我将Tor浏览器用户手册的几篇文章搬运了过来

[下载](https://tips.zhuang82.tk/gettor)

[移动 TOR](https://tips.zhuang82.tk/mobile-tor)

[网桥](https://tips.zhuang82.tk/bridges)

[规避审查](https://tips.zhuang82.tk/circumvention)

我也为大家准备了几个网桥，以彩蛋的形式出现，欢迎寻找……

### 补充

Tor Browser也是可以访问明网的，这时它的作用就类似VPN，隐藏你的真实IP。

VPN可以访问的外网Tor Browser也可以。

### 避坑指南

实际上[使用 Tor 保护自己时千万不要做这九件事！ - 哔哩哔哩 (bilibili.com)](https://www.bilibili.com/read/cv10411457/)已经讲的很详细了。为避免该文章以后再遭封杀，现镜像如下

<https://tips.zhuang82.tk/Torbk>

补充几点：

1. 少用Google的产品，否则你会遇到n多个“Are you human?”

2. 少看视频，因为网桥带宽不大

3. Tor维护不易，有钱的各位建议捐助（一定要用比特币）

4. 英语要学好，词典带身边

5. 网上有把VPN和Tor一起用的教程，普通人最好别折腾，因为安全问题（Tor project已经不推荐这种方式了）

### 法律问题

就动动眼睛不会有事的……（千万别动心）

### 后记

一张图也没有（图床容不下这些图）
