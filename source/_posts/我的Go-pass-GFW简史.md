---
title: 我的Go-pass-GFW简史
date: 2022-12-11 08:09:15
tags: ["技术","OverGFW"]
---

Go-pass-GFW是什么意思？哈哈，你懂得！话不多说，直接正文。

### 初识阶段

大概是在小学六年级时，我用Python Django做成了我人生中第一个动态网页，但动态网页需要服务器，而我当时没有钱，于是就找到了[Heroku](https://www.heroku.com/)（那时Heroku托管网页还不需要绑定信用卡），结果注册时网页总显示不能判断我是否是机器人。上网一搜，人家告诉我要翻🧱，什么是🧱呢？我当时很有疑问，但毕竟时间有限，问题被搁置了。我的第一个动态网页最终也没有部署。

### 深入阶段

初二暑假，我在同学的指导下正式了解翻🧱，首先要提到什么GFW

{% blockquote 维基百科 %}
防火长城（英語：Great Firewall，常用简称：GFW），中文也称中国国家防火墙，通常简称为墙、防火墙等，中国国家互联网信息办公室称为数据跨境安全网关，是中华人民共和国政府监控和过滤国际互联网出口内容的软硬件系统集合，用于通过技术手段，阻断不符合中国政府要求的互联网内容传输，一般认为由方滨兴主持设计。 
{% endblockquote %}


这个东西的本意是很好的，但架不住好的坏的一刀切，所以我不得已开启了Go-pass-GFW之路。

开始我使用手机，找到了[Riseup VPN](https://f-droid.org/zh_Hans/packages/se.leap.riseupvpn/)这个非常快的VPN，并用它注册了我人生中第一个外国平台的账号：[Twitter](https://twitter.com/zhuangzhuang82)

但很快我意识到，GFW也是会封VPN的，于是我来到了GitHub上，来白嫖一些免费节点，然后我找到了[freefq/free](https://github.com/freefq/free)，以及由它运营的[bulink.xyz](https://bulink.xyz/)机场，并用[v2rayNG](https://github.com/2dust/v2rayNG)应用连接

同时，我也有在电脑上翻🧱的需要，但我已有的Qv2ray已停止维护，效果不佳，之后经过一番寻找，我找到了[v2rayA](https://github.com/v2rayA/v2rayA)这个好用的代理工具，它的系统级透明代理尤为方便。

这段时间，我注册了Google，Facebook（不怎么用）。

### 自行实践阶段

突然，有一天，我在我的账户记录中发现许多异常登陆提醒，到freefq/free那边一看才发现，那些节点都是从网上通过爬虫获得的，安全性没有保障。

因为我没有钱，用不上国外的老牌VPN，我不得不主动寻找安全的方式。

首先，我要提到我从初二寒假开始加速访问GitHub的[dev-sidecar](https://github.com/docmirror/dev-sidecar)应用，我发现它居然有一个增强模式，不过是默认隐藏的，该软件作者把它做成了一个解谜游戏，点击下面的链接以开始游戏

<https://github.com/docmirror/dev-sidecar/blob/039d2e2993ec92653e7702841b74de11fa393073/packages/core/index.js>

玩得开心！～

这个增强模式使用的是域前置技术，理论上很难封锁，安全性又高，所以我现在主要用它。

不过它的增强模式带宽比较小，再加上我有对另外一个更高深的东西感兴趣，于是我发现了---

{% blockquote 维基百科 %}
Tor是实现匿名通信的自由软件。其名源于“The Onion Router”（洋葱路由器）的英语缩写。用户可透过Tor接达由全球志愿者免费提供，包含6000多个中继的覆盖网络，从而达至隐藏用户真实地址、避免网络监控及流量分析的目的。Tor用户的互联网活动（包括浏览在线网站、帖子以及即时消息等通信形式）相对较难追踪。Tor的设计原意在于保障用户的个人隐私，以及不受监控地进行秘密通信的自由和能力。  
{% endblockquote %}

通俗易懂的说，就是暗网。

进入Tor网络非常容易，只要安装Tor Browser，配置好网桥即可进入，下面有几个好用的网桥

```
obfs4 65.108.254.230:1312 A66A3B034B8A0798BC2BFFE75527D2FB2615CF3A cert=E6Y87vcmgHq94EyWpcbh+x8VuqhQOsso+oBq2VPNPus/8jXcAuJXPzJVmomh+OHJ7s5dQQ iat-mode=0
obfs4 142.4.208.107:9182 8543E63496C962DA830EDF93DB3023AA5DFB5E37 cert=luwESVwc5E2xZ1yaDm1ZtYEOJTRz9Y90+hKGKCggofX2+sYQ1IcCYJwZp58h9Uah2BaEfg iat-mode=0
obfs4 78.47.76.79:30030 C03B101F99390CABB58A0D1B04E35470E7F472F9 cert=nR4HkZtXhsutdJla5qAy3cGfJKSn/RgMloA26V72UeNlrpO65+prJ28J4w6XNRgLVBX0EQ iat-mode=0
```

以`.onion`结尾的网址为暗网网址

Tor的使用让我的浏览更加自由和方便。

本来我还想用Heroku自建节点的，但现在Heroku已经需要绑定信用卡了🤣

这段时间，我注册了Telegram。

### 总结

现在我的方案是Tor(网页)+dev-sidecar(命令行/应用程序)。

各位有更好的方案可以到评论区提出。

### 资源

1. <https://github.com/2dust/v2rayNG/releases/download/1.7.23/v2rayNG_1.7.23.apk>
2. <https://github.com/v2rayA/v2rayA/releases/download/v2.0.0/v2raya_windows_x64_2.0.0.exe>
3. <https://github.com/v2rayA/v2rayA/releases/download/v2.0.0/v2raya_darwin_x64_2.0.0>
4. <https://github.com/v2rayA/v2rayA/releases/download/v2.0.0/installer_debian_amd64_2.0.0.deb>
5. <https://github.com/docmirror/dev-sidecar/releases/download/v1.7.3/DevSidecar-1.7.3.exe>
6. <https://github.com/docmirror/dev-sidecar/releases/download/v1.7.3/DevSidecar-1.7.3.dmg>
7. <https://github.com/docmirror/dev-sidecar/releases/download/v1.7.3/DevSidecar-1.7.3.deb>
8. <https://tor.eff.org/>
9. <https://tor.calyxinstitute.org/>