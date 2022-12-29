---
title: onion
date: 2022-12-30 06:35:22
tags: ["技术","OverGFW"]
---

之前那篇Tor~，对onion还是没讲清楚。

以下内容摘编自[https://support.torproject.org/](https://support.torproject.org/)（国内无法访问）

> 只能通过 Tor 访问的网站称作“洋葱服务”，它们以 .onion 结尾。
> 比如，DuckDuckGo 的洋葱站点是 [https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/)。
> 您可以用 Tor 浏览器访问这些网站。
> 因为洋葱服务并不能像普通的网站一样被索引，所以必须由网站所有者把洋葱服务的地址分享给你。

> 洋葱服务 (旧名为“隐身服务”) 是一种只能透过洋葱路由网络访问的网络服务 (例如网站)。
> 
> 洋葱服务提供了许多架设在非私密网络空间之普通网站所没有的优势：
> 
> 洋葱服务的真实网络地址与地理位置信息被隐藏，因此很难过滤审查通往该站点之的网络连接，也很难找出该网站管理员的真实身份。
> 
> - All traffic between Tor users and onion services is end-to-end encrypted, so you do not need to worry about connecting over HTTPS.
> - 洋葱服务的网址是为自动生成，因此网站的架设者或管理员无需另行购买网络域名。其网址皆是以 .onion 结尾的，此等设计可以让洋葱路由系统确保所有网络连接都通往正确的站点，并且其连接数据未被窜改。

> 什么是客户端或洋葱认证？
> 
> 经过身份验证的洋葱服务是一种洋葱服务，它要求您在访问服务之前提供身份验证令牌（在本例中为私钥）。私钥不会传输到服务，它只用于本地解密其描述符。您可以从洋葱服务运营商处获取访问凭据。联系操作员并请求进入。了解有关如何在Tor浏览器中使用洋葱身份验证的更多信息。如果您想创建具有客户端身份验证的洋葱服务，请参阅社区门户中的客户端授权。

对于其原理，似乎也未讲清楚

根据一位网友的描述

> 前些天自己搭建了一个，其实onion是自动分配的域名。  
> 这些域名只能在TOR里面访问，很有意思的是，onion是随机分配的，onion还有一个密钥，如果这个密钥被别人知道，这个域名是可以被别人占用的。

所以onion也是用非对称性加密传输数据的，这与Https类似不过严密的多，大概与Esni(Ech)在一个级别（比他们出现的时间早得多）

但具体原理还是没说清楚，比如如何寻址

未完待续

<https://gfw.report/blog/gfw_esni_blocking/zh/>
