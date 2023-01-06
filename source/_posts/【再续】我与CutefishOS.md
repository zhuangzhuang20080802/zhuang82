---
title: 【再续】我与CutefishOS
date: 2023-01-06 15:34:37
tags: ["科技与生活","linux","CutefishOS"]
---

在上次之后，wrefiyu也终于发现了版本库的问题（好歹我提醒了他好几次），生气的在B站发了动态[wrefiyu的动态-哔哩哔哩 (bilibili.com)](https://t.bilibili.com/746110543362785314?spm_id_from=333.999.0.0)，然后被Linux中国转发，使Piscesys项目的关注度多少上升了点……

![](https://pic.imgdb.cn/item/63b7d15cbe43e0d30e54918e.jpg)

后来证明，是我们项目之前的一名开发者误操作导致的。

自此，wrefiyu决定放弃GitHub

元旦那天下午，我和wrefiyu就项目前景谈了挺长时间，再加上最近[MATSYA OS – An Evolved Fish](https://matsyaos.github.io/)的出现给了我一点灵感，就是基于Arch Linux。

我们分析了一下形势，CutefishOS(官方)没有官网论坛，yoyoos没有维护，于是我们决定先建设官网论坛。

本来我们打算借助wrefiyu小学同学刘昊宇的财力购买正规域名，但刘昊宇说他把身份证丢了，国内域名提供商要实名认证，国外的他没法支付。

于是我们考虑临时用一个免费域名代替，wrefiyu看中了.cf，因为Cutefish。

开始的官网是建在热铁盒上的，但由于wrefiyu一行行打HTML效率太低，于是我灵机一动用Hexo写了一个官网，托管在Cloudflare Pages上。

![](https://pic.imgdb.cn/item/63b7d6c7be43e0d30e62d702.jpg)

官网于1月2日开始建设，1月4日正式上线运营，网址[| Pisces System (piscesys.cf)](https://piscesys.cf/)

到现在，我都很佩服自己的聪明才智。

论坛本来不归我管，计划假设在刘昊宇个人的服务器上，结果他回老家，服务器断电了，于是我又承担起了任务，在没有VPS的情况下，使用[FreeFlarum | Sign Up](https://freeflarum.com/)搭建起了官方论坛。~~顺理成章的成了管理员~~

![](https://pic.imgdb.cn/item/63b7d8b8be43e0d30e69660b.jpg)

论坛于1月6日正式上线运营，地址<https://forums.piscesys.cf/>

总体来说，论坛还有一点冷清。

现在我的开发环境也转到了WSL上，因为Linux Mint内核太旧不识别我的显卡。

至于Jack77793说的OpenSUSE，还没时间测试。

最后还有一件事，那就是---

JingOS彻底凉了……

![](https://pic.imgdb.cn/item/63b7d22ebe43e0d30e56a274.jpg)
